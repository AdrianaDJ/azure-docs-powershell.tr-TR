---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: 171f09e2d9a9e6e646731817526451b311f94482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592409"
---
# <span data-ttu-id="0f59d-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0f59d-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="0f59d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f59d-102">SYNOPSIS</span></span>
<span data-ttu-id="0f59d-103">Yeni bir Azure Active Directory uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f59d-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f59d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f59d-104">SYNTAX</span></span>

### <span data-ttu-id="0f59d-105">ApplicationWithoutCredentialParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0f59d-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f59d-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f59d-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f59d-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f59d-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f59d-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f59d-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f59d-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f59d-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f59d-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f59d-110">DESCRIPTION</span></span>
<span data-ttu-id="0f59d-111">Yeni bir Azure Active Directory uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f59d-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="0f59d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f59d-112">EXAMPLES</span></span>

### <span data-ttu-id="0f59d-113">Yeni AAD uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0f59d-113">Create new AAD application.</span></span>
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="0f59d-114">Kimlik bilgileri olmadan yeni bir Azure Active Directory uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f59d-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="0f59d-115">Parolayla yeni AAD uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0f59d-115">Create new AAD application with password.</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="0f59d-116">Yeni bir Azure Active Directory uygulaması oluşturur ve parola kimlik bilgilerini onunla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="0f59d-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="0f59d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f59d-117">PARAMETERS</span></span>

### <span data-ttu-id="0f59d-118">-Availabletootherkiracılar</span><span class="sxs-lookup"><span data-stu-id="0f59d-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="0f59d-119">Uygulamanın tek kiracılı mı yoksa çok kiracılı mı olduğunu belirten değer.</span><span class="sxs-lookup"><span data-stu-id="0f59d-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="0f59d-120">-CertValue</span></span>
<span data-ttu-id="0f59d-121">"Asimetrik" kimlik bilgileri türü.</span><span class="sxs-lookup"><span data-stu-id="0f59d-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="0f59d-122">Temel 64 kodlu sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="0f59d-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f59d-123">-DefaultProfile</span></span>
<span data-ttu-id="0f59d-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0f59d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0f59d-125">-DisplayName</span></span>
<span data-ttu-id="0f59d-126">Yeni uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="0f59d-126">Display name of the new application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="0f59d-127">-EndDate</span></span>
<span data-ttu-id="0f59d-128">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="0f59d-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="0f59d-129">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="0f59d-129">The default end date value is one year from today.</span></span> <span data-ttu-id="0f59d-130">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0f59d-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-131">-Giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="0f59d-131">-HomePage</span></span>
<span data-ttu-id="0f59d-132">Uygulama giriş sayfasının URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="0f59d-132">The URL to the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-133">-Identifieruris</span><span class="sxs-lookup"><span data-stu-id="0f59d-133">-IdentifierUris</span></span>
<span data-ttu-id="0f59d-134">Uygulamayı tanımlayan URI 'Ler.</span><span class="sxs-lookup"><span data-stu-id="0f59d-134">The URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-135">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="0f59d-135">-KeyCredentials</span></span>
<span data-ttu-id="0f59d-136">Uygulamayla ilişkili sertifika kimlik bilgilerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="0f59d-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-137">-Parola</span><span class="sxs-lookup"><span data-stu-id="0f59d-137">-Password</span></span>
<span data-ttu-id="0f59d-138">Uygulamayla ilişkilendirilecek parola.</span><span class="sxs-lookup"><span data-stu-id="0f59d-138">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="0f59d-139">-PasswordCredentials</span></span>
<span data-ttu-id="0f59d-140">Uygulamayla ilişkili parola kimlik bilgileri listesi.</span><span class="sxs-lookup"><span data-stu-id="0f59d-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="0f59d-141">-ReplyUrls</span></span>
<span data-ttu-id="0f59d-142">Uygulama yanıt URL 'leri.</span><span class="sxs-lookup"><span data-stu-id="0f59d-142">The application reply urls.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="0f59d-143">-StartDate</span></span>
<span data-ttu-id="0f59d-144">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="0f59d-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="0f59d-145">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="0f59d-145">The default start date value is today.</span></span> <span data-ttu-id="0f59d-146">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0f59d-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="0f59d-147">-Confirm</span></span>
<span data-ttu-id="0f59d-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f59d-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f59d-149">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f59d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f59d-150">CommonParameters</span></span>
<span data-ttu-id="0f59d-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f59d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f59d-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f59d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f59d-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f59d-153">INPUTS</span></span>

### <span data-ttu-id="0f59d-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0f59d-154">None</span></span>
<span data-ttu-id="0f59d-155">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0f59d-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0f59d-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f59d-156">OUTPUTS</span></span>

### <span data-ttu-id="0f59d-157">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="0f59d-157">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="0f59d-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f59d-158">NOTES</span></span>
<span data-ttu-id="0f59d-159">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="0f59d-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0f59d-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f59d-160">RELATED LINKS</span></span>

[<span data-ttu-id="0f59d-161">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0f59d-161">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="0f59d-162">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0f59d-162">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="0f59d-163">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0f59d-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="0f59d-164">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0f59d-164">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="0f59d-165">Yeni-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0f59d-165">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="0f59d-166">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0f59d-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

