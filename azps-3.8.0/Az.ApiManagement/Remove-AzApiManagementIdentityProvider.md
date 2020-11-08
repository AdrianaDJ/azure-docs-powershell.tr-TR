---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 4909c9d9b9a7fa1af1e4353c63256ed73d229f57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097632"
---
# <span data-ttu-id="f00b0-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f00b0-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f00b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f00b0-102">SYNOPSIS</span></span>
<span data-ttu-id="f00b0-103">Var olan kimlik sağlayıcı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f00b0-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="f00b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f00b0-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f00b0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f00b0-105">DESCRIPTION</span></span>
<span data-ttu-id="f00b0-106">Var olan kimlik sağlayıcı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f00b0-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="f00b0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f00b0-107">EXAMPLES</span></span>

### <span data-ttu-id="f00b0-108">Facebook kimlik sağlayıcısı ayarlarını, Apımanayönetimi hizmetinden kaldırır</span><span class="sxs-lookup"><span data-stu-id="f00b0-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="f00b0-109">Facebook Identity Provider yapılandırması ile ilgili yapılandırmayı siler.</span><span class="sxs-lookup"><span data-stu-id="f00b0-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="f00b0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f00b0-110">PARAMETERS</span></span>

### <span data-ttu-id="f00b0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f00b0-111">-Context</span></span>
<span data-ttu-id="f00b0-112">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="f00b0-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f00b0-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f00b0-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f00b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f00b0-114">-DefaultProfile</span></span>
<span data-ttu-id="f00b0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f00b0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f00b0-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f00b0-116">-PassThru</span></span>
<span data-ttu-id="f00b0-117">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="f00b0-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="f00b0-118">-Tür</span><span class="sxs-lookup"><span data-stu-id="f00b0-118">-Type</span></span>
<span data-ttu-id="f00b0-119">Var olan bir kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f00b0-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="f00b0-120">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f00b0-120">This parameter is required.</span></span>

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

### <span data-ttu-id="f00b0-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="f00b0-121">-Confirm</span></span>
<span data-ttu-id="f00b0-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f00b0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f00b0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f00b0-123">-WhatIf</span></span>
<span data-ttu-id="f00b0-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f00b0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f00b0-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f00b0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f00b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00b0-126">CommonParameters</span></span>
<span data-ttu-id="f00b0-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f00b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f00b0-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f00b0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00b0-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f00b0-129">INPUTS</span></span>

### <span data-ttu-id="f00b0-130">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="f00b0-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f00b0-131">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovidertype</span><span class="sxs-lookup"><span data-stu-id="f00b0-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="f00b0-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f00b0-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f00b0-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f00b0-133">OUTPUTS</span></span>

### <span data-ttu-id="f00b0-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f00b0-134">System.Boolean</span></span>

## <span data-ttu-id="f00b0-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f00b0-135">NOTES</span></span>

## <span data-ttu-id="f00b0-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f00b0-136">RELATED LINKS</span></span>

[<span data-ttu-id="f00b0-137">Yeni-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="f00b0-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="f00b0-138">Get-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="f00b0-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="f00b0-139">Set-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="f00b0-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

