---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: e15e6757d6a4d0f6e84a9580877deecdeede94ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278149"
---
# <span data-ttu-id="fd185-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fd185-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="fd185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd185-102">SYNOPSIS</span></span>
<span data-ttu-id="fd185-103">Var olan kimlik sağlayıcı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fd185-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="fd185-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd185-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd185-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd185-105">DESCRIPTION</span></span>
<span data-ttu-id="fd185-106">Var olan kimlik sağlayıcı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fd185-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="fd185-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd185-107">EXAMPLES</span></span>

### <span data-ttu-id="fd185-108">Örnek 1: ıclaimana</span><span class="sxs-lookup"><span data-stu-id="fd185-108">Example 1: Removes the Facebook identity provider settings from ApiManagement service</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="fd185-109">Facebook Identity Provider yapılandırması ile ilgili yapılandırmayı siler.</span><span class="sxs-lookup"><span data-stu-id="fd185-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="fd185-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd185-110">PARAMETERS</span></span>

### <span data-ttu-id="fd185-111">-Context</span><span class="sxs-lookup"><span data-stu-id="fd185-111">-Context</span></span>
<span data-ttu-id="fd185-112">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="fd185-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fd185-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fd185-113">This parameter is required.</span></span>

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

### <span data-ttu-id="fd185-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd185-114">-DefaultProfile</span></span>
<span data-ttu-id="fd185-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd185-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd185-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fd185-116">-PassThru</span></span>
<span data-ttu-id="fd185-117">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="fd185-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="fd185-118">-Tür</span><span class="sxs-lookup"><span data-stu-id="fd185-118">-Type</span></span>
<span data-ttu-id="fd185-119">Var olan bir kimlik sağlayıcısının tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="fd185-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="fd185-120">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fd185-120">This parameter is required.</span></span>

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

### <span data-ttu-id="fd185-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd185-121">-Confirm</span></span>
<span data-ttu-id="fd185-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd185-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd185-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd185-123">-WhatIf</span></span>
<span data-ttu-id="fd185-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd185-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd185-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd185-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd185-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd185-126">CommonParameters</span></span>
<span data-ttu-id="fd185-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd185-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd185-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fd185-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd185-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd185-129">INPUTS</span></span>

### <span data-ttu-id="fd185-130">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="fd185-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fd185-131">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovidertype</span><span class="sxs-lookup"><span data-stu-id="fd185-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="fd185-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fd185-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fd185-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd185-133">OUTPUTS</span></span>

### <span data-ttu-id="fd185-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd185-134">System.Boolean</span></span>

## <span data-ttu-id="fd185-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd185-135">NOTES</span></span>

## <span data-ttu-id="fd185-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd185-136">RELATED LINKS</span></span>

[<span data-ttu-id="fd185-137">Yeni-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="fd185-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="fd185-138">Get-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="fd185-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="fd185-139">Set-Azapsananagementidentityprovider</span><span class="sxs-lookup"><span data-stu-id="fd185-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

