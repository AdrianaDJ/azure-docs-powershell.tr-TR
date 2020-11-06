---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: abfcbec55ba3f53986a63a8c0964320c10fc91ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592823"
---
# <span data-ttu-id="4ef37-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4ef37-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="4ef37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ef37-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef37-103">PsApiManagementVirtualNetwork örneğini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4ef37-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ef37-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ef37-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ef37-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ef37-105">DESCRIPTION</span></span>
<span data-ttu-id="4ef37-106">**New-AzureRmApiManagementVirtualNetwork** cmdlet 'i, bir **PsApiManagementVirtualNetwork** örneği oluşturmak için yardımcı komuttur.</span><span class="sxs-lookup"><span data-stu-id="4ef37-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="4ef37-107">Bu komut **Update-Azurermapımanagementdeployment** cmdlet 'i ile kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4ef37-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="4ef37-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ef37-108">EXAMPLES</span></span>

### <span data-ttu-id="4ef37-109">Örnek 1: sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="4ef37-109">Example 1: Create a virtual network</span></span>
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

<span data-ttu-id="4ef37-110">Bu örnekte sanal bir ağ oluşturulur ve ardından **-Azurermapımanagementdeployment** cmdlet 'ini arar.</span><span class="sxs-lookup"><span data-stu-id="4ef37-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="4ef37-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ef37-111">PARAMETERS</span></span>

### <span data-ttu-id="4ef37-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef37-112">-DefaultProfile</span></span>
<span data-ttu-id="4ef37-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ef37-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ef37-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="4ef37-114">-Location</span></span>
<span data-ttu-id="4ef37-115">API yönetim hizmeti için desteklenen bölge arasındaki konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef37-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="4ef37-116">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="4ef37-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="4ef37-117">-Subnetresourceıd</span><span class="sxs-lookup"><span data-stu-id="4ef37-117">-SubnetResourceId</span></span>
<span data-ttu-id="4ef37-118">Sanal ağın alt ağ kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef37-118">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="4ef37-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef37-119">CommonParameters</span></span>
<span data-ttu-id="4ef37-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ef37-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef37-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ef37-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef37-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ef37-122">INPUTS</span></span>

### <span data-ttu-id="4ef37-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4ef37-123">None</span></span>

## <span data-ttu-id="4ef37-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ef37-124">OUTPUTS</span></span>

### <span data-ttu-id="4ef37-125">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="4ef37-125">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="4ef37-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ef37-126">NOTES</span></span>

## <span data-ttu-id="4ef37-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ef37-127">RELATED LINKS</span></span>

[<span data-ttu-id="4ef37-128">Güncelleştirme-Azurermapımanagementdeployment</span><span class="sxs-lookup"><span data-stu-id="4ef37-128">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)

