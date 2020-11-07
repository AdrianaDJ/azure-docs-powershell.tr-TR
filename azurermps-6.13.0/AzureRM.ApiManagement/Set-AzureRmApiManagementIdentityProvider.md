---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: b7d5139abdf6404baa4abfc30b7525bfd7872174
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763921"
---
# <span data-ttu-id="70f73-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="70f73-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="70f73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70f73-102">SYNOPSIS</span></span>
<span data-ttu-id="70f73-103">Var olan bir kimlik sağlayıcısının yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="70f73-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70f73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70f73-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70f73-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70f73-105">DESCRIPTION</span></span>
<span data-ttu-id="70f73-106">Var olan bir kimlik sağlayıcısının yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="70f73-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="70f73-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70f73-107">EXAMPLES</span></span>

### <span data-ttu-id="70f73-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="70f73-108">Example 1</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="70f73-109">Cmdlet, Facebook Identity sağlayıcısının Istemci gizliliğini güncelleştirir;</span><span class="sxs-lookup"><span data-stu-id="70f73-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="70f73-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70f73-110">PARAMETERS</span></span>

### <span data-ttu-id="70f73-111">-Allowedkiracılar</span><span class="sxs-lookup"><span data-stu-id="70f73-111">-AllowedTenants</span></span>
<span data-ttu-id="70f73-112">İzin verilen Azure Active Directory kiracıları listesi.</span><span class="sxs-lookup"><span data-stu-id="70f73-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="70f73-113">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="70f73-113">-ClientId</span></span>
<span data-ttu-id="70f73-114">Dış kimlik sağlayıcısındaki uygulamanın istemci kimliği.</span><span class="sxs-lookup"><span data-stu-id="70f73-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="70f73-115">Facebook oturumu için uygulama KIMLIĞI, Google oturumu için Istemci KIMLIĞI, Microsoft için uygulama KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="70f73-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="70f73-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="70f73-116">-ClientSecret</span></span>
<span data-ttu-id="70f73-117">Dış kimlik sağlayıcısında uygulamanın, oturum açma isteğine kimlik doğrulaması için kullanılan istemci parolası.</span><span class="sxs-lookup"><span data-stu-id="70f73-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="70f73-118">Örneğin, Facebook oturumu için uygulama gizliliğine, Google Login API anahtarı, Microsoft için ortak anahtar.</span><span class="sxs-lookup"><span data-stu-id="70f73-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="70f73-119">-Context</span><span class="sxs-lookup"><span data-stu-id="70f73-119">-Context</span></span>
<span data-ttu-id="70f73-120">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="70f73-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="70f73-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="70f73-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f73-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f73-122">-DefaultProfile</span></span>
<span data-ttu-id="70f73-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70f73-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70f73-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="70f73-124">-PassThru</span></span>
<span data-ttu-id="70f73-125">Bu cmdlet 'in değiştirdiği  **Psapsananagementidentitysağlayıcısını** geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70f73-125">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f73-126">-Tür</span><span class="sxs-lookup"><span data-stu-id="70f73-126">-Type</span></span>
<span data-ttu-id="70f73-127">Var olan bir kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="70f73-127">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="70f73-128">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="70f73-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f73-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="70f73-129">-Confirm</span></span>
<span data-ttu-id="70f73-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="70f73-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70f73-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70f73-131">-WhatIf</span></span>
<span data-ttu-id="70f73-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70f73-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70f73-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="70f73-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70f73-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f73-134">CommonParameters</span></span>
<span data-ttu-id="70f73-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70f73-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f73-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70f73-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f73-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70f73-137">INPUTS</span></span>

### <span data-ttu-id="70f73-138">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="70f73-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="70f73-139">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovidertype</span><span class="sxs-lookup"><span data-stu-id="70f73-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="70f73-140">System. String</span><span class="sxs-lookup"><span data-stu-id="70f73-140">System.String</span></span>

### <span data-ttu-id="70f73-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="70f73-141">System.String[]</span></span>

### <span data-ttu-id="70f73-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="70f73-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="70f73-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70f73-143">OUTPUTS</span></span>

### <span data-ttu-id="70f73-144">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="70f73-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="70f73-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70f73-145">NOTES</span></span>

## <span data-ttu-id="70f73-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70f73-146">RELATED LINKS</span></span>

[<span data-ttu-id="70f73-147">Yeni-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="70f73-147">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="70f73-148">Get-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="70f73-148">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="70f73-149">Remove-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="70f73-149">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
