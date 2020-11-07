---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: 97ae2607484828350be67cff9c9311fc73f19b6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935483"
---
# <span data-ttu-id="59ff8-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59ff8-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="59ff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="59ff8-103">Kaynak grubunda sanal ağ alır.</span><span class="sxs-lookup"><span data-stu-id="59ff8-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="59ff8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59ff8-104">SYNTAX</span></span>

### <span data-ttu-id="59ff8-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="59ff8-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59ff8-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="59ff8-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59ff8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="59ff8-107">DESCRIPTION</span></span>
<span data-ttu-id="59ff8-108">**Get-AzVirtualNetwork** cmdlet 'i bir veya daha fazla sanal ağı bir kaynak grubuna alır.</span><span class="sxs-lookup"><span data-stu-id="59ff8-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="59ff8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59ff8-109">EXAMPLES</span></span>

### <span data-ttu-id="59ff8-110">1: sanal ağ alma</span><span class="sxs-lookup"><span data-stu-id="59ff8-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="59ff8-111">Bu komut TestResourceGroup kaynak grubunda MyVirtualNetwork adındaki sanal ağı alır</span><span class="sxs-lookup"><span data-stu-id="59ff8-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="59ff8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59ff8-112">PARAMETERS</span></span>

### <span data-ttu-id="59ff8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59ff8-113">-DefaultProfile</span></span>
<span data-ttu-id="59ff8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59ff8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59ff8-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="59ff8-115">-ExpandResource</span></span>
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

### <span data-ttu-id="59ff8-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="59ff8-116">-Name</span></span>
<span data-ttu-id="59ff8-117">Bu cmdlet 'in aldığı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59ff8-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="59ff8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59ff8-118">-ResourceGroupName</span></span>
<span data-ttu-id="59ff8-119">Sanal ağın ait olduğu kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59ff8-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="59ff8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ff8-120">CommonParameters</span></span>
<span data-ttu-id="59ff8-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59ff8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ff8-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59ff8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ff8-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59ff8-123">INPUTS</span></span>

## <span data-ttu-id="59ff8-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59ff8-124">OUTPUTS</span></span>

### <span data-ttu-id="59ff8-125">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59ff8-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="59ff8-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59ff8-126">NOTES</span></span>

## <span data-ttu-id="59ff8-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59ff8-127">RELATED LINKS</span></span>

[<span data-ttu-id="59ff8-128">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59ff8-128">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="59ff8-129">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59ff8-129">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="59ff8-130">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59ff8-130">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


