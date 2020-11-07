---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 8833d6380c14c3b2e9b9c53657602f9f3cbfd1af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753492"
---
# <span data-ttu-id="a1c73-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a1c73-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="a1c73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1c73-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c73-103">PsApiManagementVirtualNetwork örneğini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1c73-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="a1c73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1c73-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1c73-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1c73-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c73-106">**New-AzApiManagementVirtualNetwork** cmdlet 'i, bir **PsApiManagementVirtualNetwork** örneği oluşturmak için yardımcı komuttur.</span><span class="sxs-lookup"><span data-stu-id="a1c73-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="a1c73-107">Bu komut **set-Azapsanana,** **New-azapsananai** cmdlet ile kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a1c73-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="a1c73-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1c73-108">EXAMPLES</span></span>

### <span data-ttu-id="a1c73-109">Örnek 1: sanal ağ oluşturma ve mevcut bir APıM hizmetini VNET 'e güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a1c73-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="a1c73-110">Bu örnekte sanal bir ağ oluşturulur ve ardından **set-Azapsananai** cmdlet 'ini arar.</span><span class="sxs-lookup"><span data-stu-id="a1c73-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="a1c73-111">Örnek 2: dış sanal ağ için API yönetim hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="a1c73-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="a1c73-112">Bu örnek sanal ağda yeni bir APıM hizmeti oluşturur `External`</span><span class="sxs-lookup"><span data-stu-id="a1c73-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="a1c73-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1c73-113">PARAMETERS</span></span>

### <span data-ttu-id="a1c73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c73-114">-DefaultProfile</span></span>
<span data-ttu-id="a1c73-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1c73-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1c73-116">-Subnetresourceıd</span><span class="sxs-lookup"><span data-stu-id="a1c73-116">-SubnetResourceId</span></span>
<span data-ttu-id="a1c73-117">Sanal ağın alt ağ kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1c73-117">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c73-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c73-118">CommonParameters</span></span>
<span data-ttu-id="a1c73-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1c73-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c73-120">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a1c73-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c73-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1c73-121">INPUTS</span></span>

### <span data-ttu-id="a1c73-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a1c73-122">None</span></span>

## <span data-ttu-id="a1c73-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1c73-123">OUTPUTS</span></span>

### <span data-ttu-id="a1c73-124">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="a1c73-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="a1c73-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1c73-125">NOTES</span></span>

## <span data-ttu-id="a1c73-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1c73-126">RELATED LINKS</span></span>

<span data-ttu-id="a1c73-127">[Set-Azapsanana](./Set-AzApiManagement.md) 
 [Yeni-azlı](./New-AzApiManagement.md) bir</span><span class="sxs-lookup"><span data-stu-id="a1c73-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>
