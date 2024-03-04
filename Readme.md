## Introduction 

```php
 /** @var \App\Models\User */
        $user = User::factory()->make();
        $user->setTOTPSalt('salt-string'); 
        $totpService = Factory::nonRFCCompliantUserHOTP($user, 300);
        $token = $totpService->token();

        $this->assertTrue($totpService->verify($token));

```


