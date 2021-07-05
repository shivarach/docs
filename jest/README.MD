* Mock a static function
  * ```UserProfile.getUserRole = jest.fn().mockReturnValue('admin');``` or
  * ```(UserProfile.getFullName as jest.Mock).mockImplementation(() => 'John Doe');```
* Mock an exported module
 ```
 import { mocked } from 'ts-jest/utils';
 
 
 const mockAddBrand = mocked(addBrand)
 mockAddBrand.mockResolvedValueOnce(() => Promise.resolve({}));
 
 // exported in a separate file
 export const addBrand = (data: any) => api.post('/metadata/brand', data);
```
* Parametrize tests in jest
```javascript
const each = require("jest-each").default;

describe('RegulatoryGridsHelper', () => {

    each(['Singapore', 'Malaysia', 'Australia', 'New Zealand'])
        .test('should return the regulatory section "Regulatory Documents" for the region "%s"', (region: string) => {

            const regulatoryGridsForRegion = getRegulatoryGridsForRegion(regulatoryData, productMetadataWithRegulatory, region);

            expect(regulatoryGridsForRegion.length).toBe(1);
            expect(regulatoryGridsForRegion[0].gridName).toBe(REGULATORY_GRID_NAMES.REGULATORY_DOCUMENTS);
        })
      }
```
