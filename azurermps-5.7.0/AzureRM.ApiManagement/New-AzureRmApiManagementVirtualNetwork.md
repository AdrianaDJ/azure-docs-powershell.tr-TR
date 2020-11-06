---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 30a237f0f87286be8f6cd18e804d80850df7a8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595130"
---
# <span data-ttu-id="258ff-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="258ff-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="258ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="258ff-102">SYNOPSIS</span></span>
<span data-ttu-id="258ff-103">PsApiManagementVirtualNetwork örneğini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="258ff-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="258ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="258ff-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="258ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="258ff-105">DESCRIPTION</span></span>
<span data-ttu-id="258ff-106">**New-AzureRmApiManagementVirtualNetwork** cmdlet 'i, bir **PsApiManagementVirtualNetwork** örneği oluşturmak için yardımcı komuttur.</span><span class="sxs-lookup"><span data-stu-id="258ff-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="258ff-107">Bu komut **Update-Azurermapımanagementdeployment** cmdlet 'i ile kullanılır.</span><span class="sxs-lookup"><span data-stu-id="258ff-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="258ff-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="258ff-108">EXAMPLES</span></span>

### <span data-ttu-id="258ff-109">Örnek 1: sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="258ff-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzureRmvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzureRmApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzureRmApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="258ff-110">Bu örnekte sanal bir ağ oluşturulur ve ardından **-Azurermapımanagementdeployment** cmdlet 'ini arar.</span><span class="sxs-lookup"><span data-stu-id="258ff-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="258ff-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="258ff-111">PARAMETERS</span></span>

### <span data-ttu-id="258ff-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="258ff-112">-DefaultProfile</span></span>
<span data-ttu-id="258ff-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="258ff-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="258ff-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="258ff-114">-Location</span></span>
<span data-ttu-id="258ff-115">API yönetim hizmeti için desteklenen bölge arasındaki konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="258ff-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="258ff-116">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="258ff-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="258ff-117">-Subnetresourceıd</span><span class="sxs-lookup"><span data-stu-id="258ff-117">-SubnetResourceId</span></span>
<span data-ttu-id="258ff-118">Sanal ağın alt ağ kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="258ff-118">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="258ff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="258ff-119">CommonParameters</span></span>
<span data-ttu-id="258ff-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="258ff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="258ff-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="258ff-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="258ff-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="258ff-122">INPUTS</span></span>

### <span data-ttu-id="258ff-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="258ff-123">None</span></span>
<span data-ttu-id="258ff-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="258ff-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="258ff-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="258ff-125">OUTPUTS</span></span>

### <span data-ttu-id="258ff-126">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="258ff-126">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="258ff-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="258ff-127">NOTES</span></span>

## <span data-ttu-id="258ff-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="258ff-128">RELATED LINKS</span></span>

[<span data-ttu-id="258ff-129">Güncelleştirme-Azurermapımanagementdeployment</span><span class="sxs-lookup"><span data-stu-id="258ff-129">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)

