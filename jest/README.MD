* Mock a static function
  * ```UserProfile.getUserRole = jest.fn().mockReturnValue('admin');``` or
  * ```(UserProfile.getFullName as jest.Mock).mockImplementation(() => 'John Doe');```
