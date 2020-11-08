---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: a60e2b873803c8ad3acfdc08c645cf419cf8689f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104460"
---
# <span data-ttu-id="a2d25-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a2d25-101">New-AzADApplication</span></span>

## <span data-ttu-id="a2d25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2d25-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d25-103">Yeni bir Azure Active Directory uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a2d25-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="a2d25-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2d25-104">SYNTAX</span></span>

### <span data-ttu-id="a2d25-105">ApplicationWithoutCredentialParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a2d25-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d25-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2d25-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d25-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2d25-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d25-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2d25-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d25-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2d25-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2d25-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2d25-110">DESCRIPTION</span></span>
<span data-ttu-id="a2d25-111">Yeni bir Azure Active Directory uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a2d25-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="a2d25-112">Uygulama oluşturmak için gereken izinler aşağıdadır:</span><span class="sxs-lookup"><span data-stu-id="a2d25-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="a2d25-113">Azure Active Directory grafiği</span><span class="sxs-lookup"><span data-stu-id="a2d25-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="a2d25-114">Application. ReadWrite. OwnedBy</span><span class="sxs-lookup"><span data-stu-id="a2d25-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="a2d25-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="a2d25-115">Microsoft Graph</span></span>
  - <span data-ttu-id="a2d25-116">Directory. AccessAsUser. All</span><span class="sxs-lookup"><span data-stu-id="a2d25-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="a2d25-117">Dizin. ReadWrite. tümü</span><span class="sxs-lookup"><span data-stu-id="a2d25-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="a2d25-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2d25-118">EXAMPLES</span></span>

### <span data-ttu-id="a2d25-119">Örnek 1-yeni AAD uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a2d25-119">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="a2d25-120">Kimlik bilgileri olmadan yeni bir Azure Active Directory uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a2d25-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="a2d25-121">Örnek 2-parola ile yeni bir AAD uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a2d25-121">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="a2d25-122">Yeni bir Azure Active Directory uygulaması oluşturur ve parola kimlik bilgilerini onunla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="a2d25-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="a2d25-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2d25-123">PARAMETERS</span></span>

### <span data-ttu-id="a2d25-124">-Availabletootherkiracılar</span><span class="sxs-lookup"><span data-stu-id="a2d25-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="a2d25-125">Uygulamanın tek kiracılı mı yoksa çok kiracılı mı olduğunu belirten değer.</span><span class="sxs-lookup"><span data-stu-id="a2d25-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="a2d25-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="a2d25-126">-CertValue</span></span>
<span data-ttu-id="a2d25-127">"Asimetrik" kimlik bilgileri türü.</span><span class="sxs-lookup"><span data-stu-id="a2d25-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="a2d25-128">Temel 64 kodlu sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="a2d25-128">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="a2d25-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d25-129">-DefaultProfile</span></span>
<span data-ttu-id="a2d25-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a2d25-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d25-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a2d25-131">-DisplayName</span></span>
<span data-ttu-id="a2d25-132">Yeni uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="a2d25-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="a2d25-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a2d25-133">-EndDate</span></span>
<span data-ttu-id="a2d25-134">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="a2d25-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="a2d25-135">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="a2d25-135">The default end date value is one year from today.</span></span> <span data-ttu-id="a2d25-136">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a2d25-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="a2d25-137">-Giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="a2d25-137">-HomePage</span></span>
<span data-ttu-id="a2d25-138">Uygulama giriş sayfasının URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="a2d25-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="a2d25-139">-Identifieruris</span><span class="sxs-lookup"><span data-stu-id="a2d25-139">-IdentifierUris</span></span>
<span data-ttu-id="a2d25-140">Uygulamayı tanımlayan URI 'Ler.</span><span class="sxs-lookup"><span data-stu-id="a2d25-140">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="a2d25-141">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="a2d25-141">-KeyCredentials</span></span>
<span data-ttu-id="a2d25-142">Uygulamayla ilişkili sertifika kimlik bilgilerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="a2d25-142">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d25-143">-Parola</span><span class="sxs-lookup"><span data-stu-id="a2d25-143">-Password</span></span>
<span data-ttu-id="a2d25-144">Uygulamayla ilişkilendirilecek parola.</span><span class="sxs-lookup"><span data-stu-id="a2d25-144">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="a2d25-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="a2d25-145">-PasswordCredentials</span></span>
<span data-ttu-id="a2d25-146">Uygulamayla ilişkili parola kimlik bilgileri listesi.</span><span class="sxs-lookup"><span data-stu-id="a2d25-146">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d25-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="a2d25-147">-ReplyUrls</span></span>
<span data-ttu-id="a2d25-148">Uygulama yanıt URL 'leri.</span><span class="sxs-lookup"><span data-stu-id="a2d25-148">The application reply urls.</span></span>

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

### <span data-ttu-id="a2d25-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a2d25-149">-StartDate</span></span>
<span data-ttu-id="a2d25-150">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="a2d25-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="a2d25-151">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="a2d25-151">The default start date value is today.</span></span> <span data-ttu-id="a2d25-152">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a2d25-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="a2d25-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="a2d25-153">-Confirm</span></span>
<span data-ttu-id="a2d25-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a2d25-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2d25-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2d25-155">-WhatIf</span></span>
<span data-ttu-id="a2d25-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2d25-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2d25-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a2d25-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2d25-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d25-158">CommonParameters</span></span>
<span data-ttu-id="a2d25-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2d25-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d25-160">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a2d25-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d25-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2d25-161">INPUTS</span></span>

### <span data-ttu-id="a2d25-162">System. String</span><span class="sxs-lookup"><span data-stu-id="a2d25-162">System.String</span></span>

### <span data-ttu-id="a2d25-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="a2d25-163">System.String[]</span></span>

### <span data-ttu-id="a2d25-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2d25-164">System.Boolean</span></span>

### <span data-ttu-id="a2d25-165">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="a2d25-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="a2d25-166">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="a2d25-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="a2d25-167">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a2d25-167">System.Security.SecureString</span></span>

### <span data-ttu-id="a2d25-168">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="a2d25-168">System.DateTime</span></span>

## <span data-ttu-id="a2d25-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2d25-169">OUTPUTS</span></span>

### <span data-ttu-id="a2d25-170">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="a2d25-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="a2d25-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2d25-171">NOTES</span></span>
<span data-ttu-id="a2d25-172">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="a2d25-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a2d25-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2d25-173">RELATED LINKS</span></span>

[<span data-ttu-id="a2d25-174">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a2d25-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="a2d25-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a2d25-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="a2d25-176">Yeni-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a2d25-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="a2d25-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a2d25-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="a2d25-178">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a2d25-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="a2d25-179">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a2d25-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

