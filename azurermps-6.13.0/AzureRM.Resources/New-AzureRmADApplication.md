---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: e23e3db6cb574fb16b2c559c948372c808840de1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590043"
---
# <span data-ttu-id="d4b05-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d4b05-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="d4b05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4b05-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b05-103">Yeni bir Azure Active Directory uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4b05-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4b05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4b05-104">SYNTAX</span></span>

### <span data-ttu-id="d4b05-105">ApplicationWithoutCredentialParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d4b05-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b05-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4b05-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b05-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4b05-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b05-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4b05-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b05-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4b05-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4b05-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4b05-110">DESCRIPTION</span></span>
<span data-ttu-id="d4b05-111">Yeni bir Azure Active Directory uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4b05-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="d4b05-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4b05-112">EXAMPLES</span></span>

### <span data-ttu-id="d4b05-113">Örnek 1-yeni AAD uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d4b05-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="d4b05-114">Kimlik bilgileri olmadan yeni bir Azure Active Directory uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d4b05-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="d4b05-115">Örnek 2-parola ile yeni bir AAD uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d4b05-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="d4b05-116">Yeni bir Azure Active Directory uygulaması oluşturur ve parola kimlik bilgilerini onunla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="d4b05-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="d4b05-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4b05-117">PARAMETERS</span></span>

### <span data-ttu-id="d4b05-118">-Availabletootherkiracılar</span><span class="sxs-lookup"><span data-stu-id="d4b05-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="d4b05-119">Uygulamanın tek kiracılı mı yoksa çok kiracılı mı olduğunu belirten değer.</span><span class="sxs-lookup"><span data-stu-id="d4b05-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="d4b05-120">-CertValue</span></span>
<span data-ttu-id="d4b05-121">"Asimetrik" kimlik bilgileri türü.</span><span class="sxs-lookup"><span data-stu-id="d4b05-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="d4b05-122">Temel 64 kodlu sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="d4b05-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b05-123">-DefaultProfile</span></span>
<span data-ttu-id="d4b05-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d4b05-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d4b05-125">-DisplayName</span></span>
<span data-ttu-id="d4b05-126">Yeni uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="d4b05-126">Display name of the new application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d4b05-127">-EndDate</span></span>
<span data-ttu-id="d4b05-128">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="d4b05-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="d4b05-129">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="d4b05-129">The default end date value is one year from today.</span></span> <span data-ttu-id="d4b05-130">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d4b05-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-131">-Giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="d4b05-131">-HomePage</span></span>
<span data-ttu-id="d4b05-132">Uygulama giriş sayfasının URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="d4b05-132">The URL to the application homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-133">-Identifieruris</span><span class="sxs-lookup"><span data-stu-id="d4b05-133">-IdentifierUris</span></span>
<span data-ttu-id="d4b05-134">Uygulamayı tanımlayan URI 'Ler.</span><span class="sxs-lookup"><span data-stu-id="d4b05-134">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-135">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="d4b05-135">-KeyCredentials</span></span>
<span data-ttu-id="d4b05-136">Uygulamayla ilişkili sertifika kimlik bilgilerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="d4b05-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-137">-Parola</span><span class="sxs-lookup"><span data-stu-id="d4b05-137">-Password</span></span>
<span data-ttu-id="d4b05-138">Uygulamayla ilişkilendirilecek parola.</span><span class="sxs-lookup"><span data-stu-id="d4b05-138">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="d4b05-139">-PasswordCredentials</span></span>
<span data-ttu-id="d4b05-140">Uygulamayla ilişkili parola kimlik bilgileri listesi.</span><span class="sxs-lookup"><span data-stu-id="d4b05-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="d4b05-141">-ReplyUrls</span></span>
<span data-ttu-id="d4b05-142">Uygulama yanıt URL 'leri.</span><span class="sxs-lookup"><span data-stu-id="d4b05-142">The application reply urls.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="d4b05-143">-StartDate</span></span>
<span data-ttu-id="d4b05-144">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="d4b05-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="d4b05-145">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="d4b05-145">The default start date value is today.</span></span> <span data-ttu-id="d4b05-146">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d4b05-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="d4b05-147">-Confirm</span></span>
<span data-ttu-id="d4b05-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d4b05-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4b05-149">-WhatIf</span></span>
<span data-ttu-id="d4b05-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d4b05-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4b05-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d4b05-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4b05-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b05-152">CommonParameters</span></span>
<span data-ttu-id="d4b05-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4b05-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b05-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4b05-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b05-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4b05-155">INPUTS</span></span>

### <span data-ttu-id="d4b05-156">System. String</span><span class="sxs-lookup"><span data-stu-id="d4b05-156">System.String</span></span>

### <span data-ttu-id="d4b05-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="d4b05-157">System.String[]</span></span>

### <span data-ttu-id="d4b05-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4b05-158">System.Boolean</span></span>

### <span data-ttu-id="d4b05-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="d4b05-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="d4b05-160">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="d4b05-160">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="d4b05-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="d4b05-161">System.Security.SecureString</span></span>

### <span data-ttu-id="d4b05-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="d4b05-162">System.DateTime</span></span>

## <span data-ttu-id="d4b05-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4b05-163">OUTPUTS</span></span>

### <span data-ttu-id="d4b05-164">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d4b05-164">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="d4b05-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4b05-165">NOTES</span></span>
<span data-ttu-id="d4b05-166">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="d4b05-166">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d4b05-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4b05-167">RELATED LINKS</span></span>

[<span data-ttu-id="d4b05-168">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d4b05-168">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="d4b05-169">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d4b05-169">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="d4b05-170">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d4b05-170">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="d4b05-171">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d4b05-171">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="d4b05-172">Yeni-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d4b05-172">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="d4b05-173">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d4b05-173">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

