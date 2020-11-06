---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: d955cb51d92d9d0f3c156900d847e903d642e9af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591100"
---
# <span data-ttu-id="957ac-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="957ac-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="957ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="957ac-102">SYNOPSIS</span></span>
<span data-ttu-id="957ac-103">Kaynak grubunda sanal ağ alır.</span><span class="sxs-lookup"><span data-stu-id="957ac-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="957ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="957ac-104">SYNTAX</span></span>

### <span data-ttu-id="957ac-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="957ac-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="957ac-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="957ac-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="957ac-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="957ac-107">DESCRIPTION</span></span>
<span data-ttu-id="957ac-108">**Get-AzureRmVirtualNetwork** cmdlet 'i bir veya daha fazla sanal ağı bir kaynak grubuna alır.</span><span class="sxs-lookup"><span data-stu-id="957ac-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="957ac-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="957ac-109">EXAMPLES</span></span>

### <span data-ttu-id="957ac-110">1: sanal ağ alma</span><span class="sxs-lookup"><span data-stu-id="957ac-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="957ac-111">Bu komut TestResourceGroup kaynak grubunda MyVirtualNetwork adındaki sanal ağı alır</span><span class="sxs-lookup"><span data-stu-id="957ac-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="957ac-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="957ac-112">PARAMETERS</span></span>

### <span data-ttu-id="957ac-113">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="957ac-113">-ExpandResource</span></span>
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

### <span data-ttu-id="957ac-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="957ac-114">-Name</span></span>
<span data-ttu-id="957ac-115">Bu cmdlet 'in aldığı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="957ac-115">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="957ac-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="957ac-116">-ResourceGroupName</span></span>
<span data-ttu-id="957ac-117">Sanal ağın ait olduğu kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="957ac-117">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="957ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="957ac-118">-DefaultProfile</span></span>
<span data-ttu-id="957ac-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="957ac-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="957ac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957ac-120">CommonParameters</span></span>
<span data-ttu-id="957ac-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="957ac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957ac-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="957ac-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957ac-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="957ac-123">INPUTS</span></span>

## <span data-ttu-id="957ac-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="957ac-124">OUTPUTS</span></span>

### <span data-ttu-id="957ac-125">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="957ac-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="957ac-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="957ac-126">NOTES</span></span>

## <span data-ttu-id="957ac-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="957ac-127">RELATED LINKS</span></span>

[<span data-ttu-id="957ac-128">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="957ac-128">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="957ac-129">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="957ac-129">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="957ac-130">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="957ac-130">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


