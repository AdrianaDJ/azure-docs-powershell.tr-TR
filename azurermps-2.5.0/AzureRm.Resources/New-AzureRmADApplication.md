---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: 71e5e6c3cc80235b68df5c90e95a96e760abf80b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939671"
---
# <span data-ttu-id="5e4f1-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5e4f1-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="5e4f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e4f1-102">SYNOPSIS</span></span>
<span data-ttu-id="5e4f1-103">Yeni bir Azure Active Directory uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e4f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e4f1-104">SYNTAX</span></span>

### <span data-ttu-id="5e4f1-105">ApplicationWithoutCredentialParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5e4f1-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e4f1-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e4f1-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e4f1-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e4f1-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e4f1-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e4f1-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e4f1-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e4f1-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e4f1-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e4f1-110">DESCRIPTION</span></span>
<span data-ttu-id="5e4f1-111">Yeni bir Azure Active Directory uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="5e4f1-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e4f1-112">EXAMPLES</span></span>

### <span data-ttu-id="5e4f1-113">Örnek 1-yeni AAD uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="5e4f1-114">Kimlik bilgileri olmadan yeni bir Azure Active Directory uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="5e4f1-115">Örnek 2-parola ile yeni bir AAD uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="5e4f1-116">Yeni bir Azure Active Directory uygulaması oluşturur ve parola kimlik bilgilerini onunla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="5e4f1-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e4f1-117">PARAMETERS</span></span>

### <span data-ttu-id="5e4f1-118">-Availabletootherkiracılar</span><span class="sxs-lookup"><span data-stu-id="5e4f1-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="5e4f1-119">Uygulamanın tek kiracılı mı yoksa çok kiracılı mı olduğunu belirten değer.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="5e4f1-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="5e4f1-120">-CertValue</span></span>
<span data-ttu-id="5e4f1-121">"Asimetrik" kimlik bilgileri türü.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="5e4f1-122">Temel 64 kodlu sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="5e4f1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e4f1-123">-DefaultProfile</span></span>
<span data-ttu-id="5e4f1-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5e4f1-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e4f1-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5e4f1-125">-DisplayName</span></span>
<span data-ttu-id="5e4f1-126">Yeni uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-126">Display name of the new application.</span></span>

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

### <span data-ttu-id="5e4f1-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="5e4f1-127">-EndDate</span></span>
<span data-ttu-id="5e4f1-128">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="5e4f1-129">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-129">The default end date value is one year from today.</span></span> <span data-ttu-id="5e4f1-130">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="5e4f1-131">-Giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="5e4f1-131">-HomePage</span></span>
<span data-ttu-id="5e4f1-132">Uygulama giriş sayfasının URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-132">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="5e4f1-133">-Identifieruris</span><span class="sxs-lookup"><span data-stu-id="5e4f1-133">-IdentifierUris</span></span>
<span data-ttu-id="5e4f1-134">Uygulamayı tanımlayan URI 'Ler.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-134">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="5e4f1-135">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="5e4f1-135">-KeyCredentials</span></span>
<span data-ttu-id="5e4f1-136">Uygulamayla ilişkili sertifika kimlik bilgilerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-136">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="5e4f1-137">-Parola</span><span class="sxs-lookup"><span data-stu-id="5e4f1-137">-Password</span></span>
<span data-ttu-id="5e4f1-138">Uygulamayla ilişkilendirilecek parola.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-138">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="5e4f1-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="5e4f1-139">-PasswordCredentials</span></span>
<span data-ttu-id="5e4f1-140">Uygulamayla ilişkili parola kimlik bilgileri listesi.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-140">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="5e4f1-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="5e4f1-141">-ReplyUrls</span></span>
<span data-ttu-id="5e4f1-142">Uygulama yanıt URL 'leri.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-142">The application reply urls.</span></span>

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

### <span data-ttu-id="5e4f1-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="5e4f1-143">-StartDate</span></span>
<span data-ttu-id="5e4f1-144">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="5e4f1-145">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-145">The default start date value is today.</span></span> <span data-ttu-id="5e4f1-146">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="5e4f1-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e4f1-147">-Confirm</span></span>
<span data-ttu-id="5e4f1-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e4f1-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e4f1-149">-WhatIf</span></span>
<span data-ttu-id="5e4f1-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e4f1-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e4f1-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e4f1-152">CommonParameters</span></span>
<span data-ttu-id="5e4f1-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e4f1-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e4f1-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e4f1-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e4f1-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e4f1-155">INPUTS</span></span>

### <span data-ttu-id="5e4f1-156">System. String</span><span class="sxs-lookup"><span data-stu-id="5e4f1-156">System.String</span></span>

### <span data-ttu-id="5e4f1-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="5e4f1-157">System.String[]</span></span>

### <span data-ttu-id="5e4f1-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e4f1-158">System.Boolean</span></span>

### <span data-ttu-id="5e4f1-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="5e4f1-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="5e4f1-160">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="5e4f1-160">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="5e4f1-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="5e4f1-161">System.Security.SecureString</span></span>

### <span data-ttu-id="5e4f1-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="5e4f1-162">System.DateTime</span></span>

## <span data-ttu-id="5e4f1-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e4f1-163">OUTPUTS</span></span>

### <span data-ttu-id="5e4f1-164">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="5e4f1-164">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="5e4f1-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e4f1-165">NOTES</span></span>
<span data-ttu-id="5e4f1-166">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="5e4f1-166">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5e4f1-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e4f1-167">RELATED LINKS</span></span>

[<span data-ttu-id="5e4f1-168">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5e4f1-168">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="5e4f1-169">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5e4f1-169">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="5e4f1-170">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5e4f1-170">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="5e4f1-171">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5e4f1-171">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="5e4f1-172">Yeni-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5e4f1-172">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="5e4f1-173">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5e4f1-173">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

