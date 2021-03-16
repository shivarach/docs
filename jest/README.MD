* Mock a static function
  * ```UserProfile.getUserRole = jest.fn().mockReturnValue('admin');``` or
  * ```(UserProfile.getFullName as jest.Mock).mockImplementation(() => 'John Doe');```
* Mock an exported module
 ```
 const mockAddBrand = mocked(addBrand)
 mockAddBrand.mockResolvedValueOnce(() => Promise.resolve({}));
 
 // exported in a separate file
 export const addBrand = (data: any) => api.post('/metadata/brand', data);
```
