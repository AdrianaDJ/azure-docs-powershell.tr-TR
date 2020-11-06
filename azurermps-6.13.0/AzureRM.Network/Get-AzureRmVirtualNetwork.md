---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: 3a5cd755718536170c3e6fb1f6dd5410e1acffc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595073"
---
# <span data-ttu-id="df917-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df917-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="df917-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df917-102">SYNOPSIS</span></span>
<span data-ttu-id="df917-103">Kaynak grubunda sanal ağ alır.</span><span class="sxs-lookup"><span data-stu-id="df917-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df917-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df917-104">SYNTAX</span></span>

### <span data-ttu-id="df917-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="df917-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df917-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="df917-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df917-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="df917-107">DESCRIPTION</span></span>
<span data-ttu-id="df917-108">**Get-AzureRmVirtualNetwork** cmdlet 'i bir veya daha fazla sanal ağı bir kaynak grubuna alır.</span><span class="sxs-lookup"><span data-stu-id="df917-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="df917-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df917-109">EXAMPLES</span></span>

### <span data-ttu-id="df917-110">1: sanal ağ alma</span><span class="sxs-lookup"><span data-stu-id="df917-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="df917-111">Bu komut TestResourceGroup kaynak grubunda MyVirtualNetwork adındaki sanal ağı alır</span><span class="sxs-lookup"><span data-stu-id="df917-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="df917-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df917-112">PARAMETERS</span></span>

### <span data-ttu-id="df917-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df917-113">-DefaultProfile</span></span>
<span data-ttu-id="df917-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df917-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df917-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="df917-115">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df917-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="df917-116">-Name</span></span>
<span data-ttu-id="df917-117">Bu cmdlet 'in aldığı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df917-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df917-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df917-118">-ResourceGroupName</span></span>
<span data-ttu-id="df917-119">Sanal ağın ait olduğu kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df917-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df917-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df917-120">CommonParameters</span></span>
<span data-ttu-id="df917-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df917-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df917-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df917-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df917-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df917-123">INPUTS</span></span>

### <span data-ttu-id="df917-124">System. String</span><span class="sxs-lookup"><span data-stu-id="df917-124">System.String</span></span>

## <span data-ttu-id="df917-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df917-125">OUTPUTS</span></span>

### <span data-ttu-id="df917-126">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df917-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="df917-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df917-127">NOTES</span></span>

## <span data-ttu-id="df917-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df917-128">RELATED LINKS</span></span>

[<span data-ttu-id="df917-129">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df917-129">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="df917-130">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df917-130">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="df917-131">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df917-131">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


