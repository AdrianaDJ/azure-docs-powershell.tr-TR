---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d8cc54570b1282889a93c803e1216096cde35b27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573034"
---
# <span data-ttu-id="cabd3-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="cabd3-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="cabd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cabd3-102">SYNOPSIS</span></span>
<span data-ttu-id="cabd3-103">Var olan kimlik sağlayıcı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cabd3-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cabd3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cabd3-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cabd3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cabd3-105">DESCRIPTION</span></span>
<span data-ttu-id="cabd3-106">Var olan kimlik sağlayıcı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cabd3-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="cabd3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cabd3-107">EXAMPLES</span></span>

### <span data-ttu-id="cabd3-108">Facebook kimlik sağlayıcısı ayarlarını, Apımanayönetimi hizmetinden kaldırır</span><span class="sxs-lookup"><span data-stu-id="cabd3-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="cabd3-109">Facebook Identity Provider yapılandırması ile ilgili yapılandırmayı siler.</span><span class="sxs-lookup"><span data-stu-id="cabd3-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="cabd3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cabd3-110">PARAMETERS</span></span>

### <span data-ttu-id="cabd3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="cabd3-111">-Context</span></span>
<span data-ttu-id="cabd3-112">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="cabd3-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cabd3-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="cabd3-113">This parameter is required.</span></span>

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

### <span data-ttu-id="cabd3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cabd3-114">-DefaultProfile</span></span>
<span data-ttu-id="cabd3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cabd3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cabd3-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cabd3-116">-PassThru</span></span>
<span data-ttu-id="cabd3-117">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="cabd3-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="cabd3-118">-Tür</span><span class="sxs-lookup"><span data-stu-id="cabd3-118">-Type</span></span>
<span data-ttu-id="cabd3-119">Var olan bir kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="cabd3-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="cabd3-120">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="cabd3-120">This parameter is required.</span></span>

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

### <span data-ttu-id="cabd3-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="cabd3-121">-Confirm</span></span>
<span data-ttu-id="cabd3-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cabd3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cabd3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cabd3-123">-WhatIf</span></span>
<span data-ttu-id="cabd3-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cabd3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cabd3-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cabd3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cabd3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cabd3-126">CommonParameters</span></span>
<span data-ttu-id="cabd3-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cabd3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cabd3-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cabd3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cabd3-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cabd3-129">INPUTS</span></span>

### <span data-ttu-id="cabd3-130">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="cabd3-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cabd3-131">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovidertype</span><span class="sxs-lookup"><span data-stu-id="cabd3-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="cabd3-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cabd3-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cabd3-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cabd3-133">OUTPUTS</span></span>

### <span data-ttu-id="cabd3-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cabd3-134">System.Boolean</span></span>

## <span data-ttu-id="cabd3-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cabd3-135">NOTES</span></span>

## <span data-ttu-id="cabd3-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cabd3-136">RELATED LINKS</span></span>

[<span data-ttu-id="cabd3-137">Yeni-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="cabd3-137">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="cabd3-138">Get-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="cabd3-138">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="cabd3-139">Set-Azurermapımanagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="cabd3-139">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

