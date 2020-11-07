---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: c33bf796336bb039ae6e68ab24769e1375cc1a4e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936410"
---
# <span data-ttu-id="7f9a8-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7f9a8-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="7f9a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f9a8-102">SYNOPSIS</span></span>
<span data-ttu-id="7f9a8-103">Var olan bir uygulamaya kimlik bilgisi ekler.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="7f9a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f9a8-104">SYNTAX</span></span>

### <span data-ttu-id="7f9a8-105">Applicationobjectivseçwithpasswordparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7f9a8-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f9a8-106">Applicationobjectivseçwithcertvalueparameterset</span><span class="sxs-lookup"><span data-stu-id="7f9a8-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f9a8-107">Applicationıdwithcertvalueparameterset</span><span class="sxs-lookup"><span data-stu-id="7f9a8-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f9a8-108">Applicationıdwithpasswordparameterset</span><span class="sxs-lookup"><span data-stu-id="7f9a8-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f9a8-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f9a8-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f9a8-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f9a8-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f9a8-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f9a8-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f9a8-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f9a8-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f9a8-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f9a8-113">DESCRIPTION</span></span>
<span data-ttu-id="7f9a8-114">New-AzADAppCredential cmdlet 'i, bir uygulamanın yeni kimlik bilgilerini almak veya kimlik bilgilerini almak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="7f9a8-115">Uygulama, uygulama nesnesi kimliği veya uygulama kimliği sağlayarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="7f9a8-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f9a8-116">EXAMPLES</span></span>

### <span data-ttu-id="7f9a8-117">Örnek 1-parola kullanarak yeni bir uygulama kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7f9a8-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="7f9a8-118">' 1f89cf81-0146-4f4e-PE-2007d0668416 ' nesne kimliğine sahip mevcut uygulama kimlik bilgileri yeni bir parola ile eklenir.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-118">A new password credential is added to the existing appplication with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="7f9a8-119">Örnek 2-sertifika kullanarak yeni bir uygulama kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7f9a8-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 
PS C:\> $cer.Import("C:\myapp.cer") 
PS C:\> $binCert = $cer.GetRawCertData() 
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="7f9a8-120">Sağlanan base64 kodlu genel x509 sertifikası ("MyApp. cer"), ' 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 ' uygulama kimliğiyle var olan uygulamaya eklenir.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="7f9a8-121">Örnek 3-boru kullanarak yeni bir uygulama kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7f9a8-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="7f9a8-122">Nesne kimliği ' 1f89cf81-0146-4f4e-Dee-2007vseç0668416 ' ile uygulamayı alır ve bu uygulama için belirtilen parolayla yeni bir uygulama kimlik bilgisi oluşturmak için New-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="7f9a8-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f9a8-123">PARAMETERS</span></span>

### <span data-ttu-id="7f9a8-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7f9a8-124">-ApplicationId</span></span>
<span data-ttu-id="7f9a8-125">Kimlik bilgilerinin ekleneceği uygulamanın uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-125">The application id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a8-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="7f9a8-126">-ApplicationObject</span></span>
<span data-ttu-id="7f9a8-127">Kimlik bilgilerinin ekleneceği uygulama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-127">The application object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithCertValueParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a8-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="7f9a8-128">-CertValue</span></span>
<span data-ttu-id="7f9a8-129">"Asimetrik" kimlik bilgileri türü.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="7f9a8-130">Temel 64 kodlu sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-130">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithCertValueParameterSet, ApplicationObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f9a8-131">-DefaultProfile</span></span>
<span data-ttu-id="7f9a8-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7f9a8-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a8-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7f9a8-133">-DisplayName</span></span>
<span data-ttu-id="7f9a8-134">Uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-134">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithPasswordParameterSet, DisplayNameWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a8-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="7f9a8-135">-EndDate</span></span>
<span data-ttu-id="7f9a8-136">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="7f9a8-137">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="7f9a8-138">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a8-139">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="7f9a8-139">-ObjectId</span></span>
<span data-ttu-id="7f9a8-140">Kimlik bilgilerinin ekleneceği uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-140">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a8-141">-Parola</span><span class="sxs-lookup"><span data-stu-id="7f9a8-141">-Password</span></span>
<span data-ttu-id="7f9a8-142">Uygulamayla ilişkilendirilecek parola.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-142">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: DisplayNameWithPasswordParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a8-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="7f9a8-143">-StartDate</span></span>
<span data-ttu-id="7f9a8-144">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="7f9a8-145">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-145">The default start date value is today.</span></span> <span data-ttu-id="7f9a8-146">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a8-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f9a8-147">-Confirm</span></span>
<span data-ttu-id="7f9a8-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a8-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f9a8-149">-WhatIf</span></span>
<span data-ttu-id="7f9a8-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f9a8-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f9a8-152">CommonParameters</span></span>
<span data-ttu-id="7f9a8-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f9a8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f9a8-154">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f9a8-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f9a8-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f9a8-155">INPUTS</span></span>

### <span data-ttu-id="7f9a8-156">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7f9a8-156">System.Guid</span></span>

### <span data-ttu-id="7f9a8-157">System. String</span><span class="sxs-lookup"><span data-stu-id="7f9a8-157">System.String</span></span>

### <span data-ttu-id="7f9a8-158">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7f9a8-158">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="7f9a8-159">Parametreler: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7f9a8-159">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="7f9a8-160">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="7f9a8-160">System.Security.SecureString</span></span>

### <span data-ttu-id="7f9a8-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="7f9a8-161">System.DateTime</span></span>

## <span data-ttu-id="7f9a8-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f9a8-162">OUTPUTS</span></span>

### <span data-ttu-id="7f9a8-163">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="7f9a8-163">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="7f9a8-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f9a8-164">NOTES</span></span>

## <span data-ttu-id="7f9a8-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f9a8-165">RELATED LINKS</span></span>

[<span data-ttu-id="7f9a8-166">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7f9a8-166">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="7f9a8-167">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7f9a8-167">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="7f9a8-168">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7f9a8-168">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

