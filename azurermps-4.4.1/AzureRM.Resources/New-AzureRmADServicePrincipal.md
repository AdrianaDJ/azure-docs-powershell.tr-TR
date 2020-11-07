---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: 4b327193a8dcbfecae8f13fa234da703d1a93cfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764784"
---
# <span data-ttu-id="8ea8b-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8ea8b-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="8ea8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ea8b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea8b-103">Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ea8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ea8b-104">SYNTAX</span></span>

### <span data-ttu-id="8ea8b-105">ApplicationWithoutCredentialParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8ea8b-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ea8b-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea8b-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ea8b-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea8b-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ea8b-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea8b-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ea8b-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea8b-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ea8b-110">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea8b-110">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ea8b-111">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea8b-111">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ea8b-112">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea8b-112">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ea8b-113">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea8b-113">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ea8b-114">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea8b-114">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ea8b-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ea8b-115">DESCRIPTION</span></span>
<span data-ttu-id="8ea8b-116">Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-116">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="8ea8b-117">Not: cmdlet Ayrıca bir uygulama oluşturur ve özelliklerini (ApplicationId sağlanmadıysa) ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-117">Note: The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span>
<span data-ttu-id="8ea8b-118">Uygulamaya özgü parametreleri güncelleştirmek için lütfen Set-AzureRmADApplication cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-118">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="8ea8b-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ea8b-119">EXAMPLES</span></span>

### <span data-ttu-id="8ea8b-120">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ea8b-120">--------------------------  Example 1  --------------------------</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
```

<span data-ttu-id="8ea8b-121">Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-121">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="8ea8b-122">DisplayName türü ObjectID</span><span class="sxs-lookup"><span data-stu-id="8ea8b-122">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="8ea8b-123">DemoApp ServicePrincipal f95b6f5c-fc98-4AF0-bb8a-34a14ca1dca1</span><span class="sxs-lookup"><span data-stu-id="8ea8b-123">DemoApp                        ServicePrincipal               f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span></span>

### <span data-ttu-id="8ea8b-124">--------------------------Örnek 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ea8b-124">--------------------------  Example 2  --------------------------</span></span>
```
New-AzureRmADServicePrincipal -DisplayName SPForNoExistingApp
```

<span data-ttu-id="8ea8b-125">Yeni bir hizmet sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-125">Creates a new service principal.</span></span>
<span data-ttu-id="8ea8b-126">Cmdlet, sağlanmadığından da örtülü olarak bir uygulama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-126">The cmdlet also implicitly creates an application since one is not provided.</span></span>

<span data-ttu-id="8ea8b-127">DisplayName türü ObjectID</span><span class="sxs-lookup"><span data-stu-id="8ea8b-127">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="8ea8b-128">SPForNoExistingApp ServicePrincipal 784136ca-3ae2-4fdd-A388-89vseç993e7c780</span><span class="sxs-lookup"><span data-stu-id="8ea8b-128">SPForNoExistingApp             ServicePrincipal               784136ca-3ae2-4fdd-a388-89d993e7c780</span></span>

## <span data-ttu-id="8ea8b-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ea8b-129">PARAMETERS</span></span>

### <span data-ttu-id="8ea8b-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8ea8b-130">-ApplicationId</span></span>
<span data-ttu-id="8ea8b-131">Kiracıdaki bir hizmet sorumlusunun benzersiz uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-131">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="8ea8b-132">Bu özellik, oluşturulduktan sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-132">Once created this property cannot be changed.</span></span>
<span data-ttu-id="8ea8b-133">Uygulama kimliği belirtilmezse, bir tane oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-133">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea8b-134">-CertValue</span><span class="sxs-lookup"><span data-stu-id="8ea8b-134">-CertValue</span></span>
<span data-ttu-id="8ea8b-135">"Asimetrik" kimlik bilgileri türü.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-135">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="8ea8b-136">Temel 64 kodlu sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-136">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea8b-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8ea8b-137">-DisplayName</span></span>
<span data-ttu-id="8ea8b-138">Hizmet sorumlusunun kolay adı.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-138">The friendly name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea8b-139">-EndDate</span><span class="sxs-lookup"><span data-stu-id="8ea8b-139">-EndDate</span></span>
<span data-ttu-id="8ea8b-140">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-140">The effective end date of the credential usage.</span></span>
<span data-ttu-id="8ea8b-141">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-141">The default end date value is one year from today.</span></span> <span data-ttu-id="8ea8b-142">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-142">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea8b-143">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="8ea8b-143">-KeyCredentials</span></span>
<span data-ttu-id="8ea8b-144">Hizmet sorumlusu ile ilişkili sertifika kimlik bilgilerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-144">The list of certificate credentials associated with the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea8b-145">-Parola</span><span class="sxs-lookup"><span data-stu-id="8ea8b-145">-Password</span></span>
<span data-ttu-id="8ea8b-146">Hizmet sorumlusu ile ilişkilendirilecek parola.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-146">The password to be associated with the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea8b-147">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="8ea8b-147">-PasswordCredentials</span></span>
<span data-ttu-id="8ea8b-148">Hizmet sorumlusu ile ilişkili parola kimlik bilgileri listesi.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-148">The list of password credentials associated with the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea8b-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="8ea8b-149">-StartDate</span></span>
<span data-ttu-id="8ea8b-150">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="8ea8b-151">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-151">The default start date value is today.</span></span> <span data-ttu-id="8ea8b-152">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea8b-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="8ea8b-153">-Confirm</span></span>
<span data-ttu-id="8ea8b-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ea8b-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ea8b-155">-WhatIf</span></span>
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

### <span data-ttu-id="8ea8b-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea8b-156">-DefaultProfile</span></span>
<span data-ttu-id="8ea8b-157">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ea8b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea8b-158">CommonParameters</span></span>
<span data-ttu-id="8ea8b-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ea8b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea8b-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ea8b-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea8b-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ea8b-161">INPUTS</span></span>

## <span data-ttu-id="8ea8b-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ea8b-162">OUTPUTS</span></span>

### <span data-ttu-id="8ea8b-163">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8ea8b-163">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="8ea8b-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ea8b-164">NOTES</span></span>
<span data-ttu-id="8ea8b-165">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="8ea8b-165">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="8ea8b-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ea8b-166">RELATED LINKS</span></span>

[<span data-ttu-id="8ea8b-167">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8ea8b-167">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="8ea8b-168">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8ea8b-168">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="8ea8b-169">Yeni-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="8ea8b-169">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="8ea8b-170">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="8ea8b-170">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="8ea8b-171">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8ea8b-171">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="8ea8b-172">Yeni-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8ea8b-172">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="8ea8b-173">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8ea8b-173">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)
