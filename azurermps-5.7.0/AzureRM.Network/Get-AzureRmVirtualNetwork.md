---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: 1745e3a87d91917e762c9b0e441110b4b6945601
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588171"
---
# <span data-ttu-id="ce42e-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ce42e-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="ce42e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce42e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce42e-103">Kaynak grubunda sanal ağ alır.</span><span class="sxs-lookup"><span data-stu-id="ce42e-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce42e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce42e-104">SYNTAX</span></span>

### <span data-ttu-id="ce42e-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="ce42e-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce42e-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="ce42e-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce42e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce42e-107">DESCRIPTION</span></span>
<span data-ttu-id="ce42e-108">**Get-AzureRmVirtualNetwork** cmdlet 'i bir veya daha fazla sanal ağı bir kaynak grubuna alır.</span><span class="sxs-lookup"><span data-stu-id="ce42e-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="ce42e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce42e-109">EXAMPLES</span></span>

### <span data-ttu-id="ce42e-110">1: sanal ağ alma</span><span class="sxs-lookup"><span data-stu-id="ce42e-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="ce42e-111">Bu komut TestResourceGroup kaynak grubunda MyVirtualNetwork adındaki sanal ağı alır</span><span class="sxs-lookup"><span data-stu-id="ce42e-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="ce42e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce42e-112">PARAMETERS</span></span>

### <span data-ttu-id="ce42e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce42e-113">-DefaultProfile</span></span>
<span data-ttu-id="ce42e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce42e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce42e-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ce42e-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce42e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ce42e-116">-Name</span></span>
<span data-ttu-id="ce42e-117">Bu cmdlet 'in aldığı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce42e-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce42e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce42e-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce42e-119">Sanal ağın ait olduğu kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce42e-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce42e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce42e-120">CommonParameters</span></span>
<span data-ttu-id="ce42e-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce42e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce42e-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce42e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce42e-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce42e-123">INPUTS</span></span>

### <span data-ttu-id="ce42e-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ce42e-124">None</span></span>
<span data-ttu-id="ce42e-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ce42e-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ce42e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce42e-126">OUTPUTS</span></span>

### <span data-ttu-id="ce42e-127">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ce42e-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ce42e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce42e-128">NOTES</span></span>

## <span data-ttu-id="ce42e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce42e-129">RELATED LINKS</span></span>

[<span data-ttu-id="ce42e-130">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ce42e-130">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="ce42e-131">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ce42e-131">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="ce42e-132">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ce42e-132">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


