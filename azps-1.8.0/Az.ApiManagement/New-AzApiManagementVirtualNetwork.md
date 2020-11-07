---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 67020f99129dfa920aa1bbc5e22ac59c16affb32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917819"
---
# <span data-ttu-id="5bba9-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5bba9-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="5bba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bba9-102">SYNOPSIS</span></span>
<span data-ttu-id="5bba9-103">PsApiManagementVirtualNetwork örneğini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5bba9-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="5bba9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5bba9-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bba9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5bba9-105">DESCRIPTION</span></span>
<span data-ttu-id="5bba9-106">**New-AzApiManagementVirtualNetwork** cmdlet 'i, bir **PsApiManagementVirtualNetwork** örneği oluşturmak için yardımcı komuttur.</span><span class="sxs-lookup"><span data-stu-id="5bba9-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="5bba9-107">Bu komut, **Update-Azapsananagementdeployment** cmdlet ile kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5bba9-107">This command is used with **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="5bba9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5bba9-108">EXAMPLES</span></span>

### <span data-ttu-id="5bba9-109">Örnek 1: sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="5bba9-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="5bba9-110">Bu örnekte sanal bir ağ oluşturulur ve ardından **Update-Azapsananagementdeployment** cmdlet 'i arar.</span><span class="sxs-lookup"><span data-stu-id="5bba9-110">This example creates a virtual network and then calls the **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="5bba9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5bba9-111">PARAMETERS</span></span>

### <span data-ttu-id="5bba9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bba9-112">-DefaultProfile</span></span>
<span data-ttu-id="5bba9-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5bba9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bba9-114">-Subnetresourceıd</span><span class="sxs-lookup"><span data-stu-id="5bba9-114">-SubnetResourceId</span></span>
<span data-ttu-id="5bba9-115">Sanal ağın alt ağ kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bba9-115">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="5bba9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bba9-116">CommonParameters</span></span>
<span data-ttu-id="5bba9-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5bba9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bba9-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bba9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bba9-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5bba9-119">INPUTS</span></span>

### <span data-ttu-id="5bba9-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5bba9-120">None</span></span>

## <span data-ttu-id="5bba9-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5bba9-121">OUTPUTS</span></span>

### <span data-ttu-id="5bba9-122">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="5bba9-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="5bba9-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5bba9-123">NOTES</span></span>

## <span data-ttu-id="5bba9-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5bba9-124">RELATED LINKS</span></span>

[<span data-ttu-id="5bba9-125">Güncelleştirme-Azapsananagementdeployment</span><span class="sxs-lookup"><span data-stu-id="5bba9-125">Update-AzApiManagementDeployment</span></span>](./Update-AzApiManagementDeployment.md)
