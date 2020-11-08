---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 37c9827f2af970c0c376c31f4d67ba7723e02e99
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935562"
---
# <span data-ttu-id="25cd4-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="25cd4-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="25cd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25cd4-102">SYNOPSIS</span></span>
<span data-ttu-id="25cd4-103">Ağ arabiriminin etkin yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="25cd4-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="25cd4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25cd4-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25cd4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="25cd4-105">DESCRIPTION</span></span>
<span data-ttu-id="25cd4-106">**Get-AzEffectiveRouteTable** cmdlet 'i, bir ağ arabirimine uygulanan etkin yol tablosunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="25cd4-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="25cd4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25cd4-107">EXAMPLES</span></span>

### <span data-ttu-id="25cd4-108">Örnek 1: ağ arabiriminde etkin yol tablosunu alma</span><span class="sxs-lookup"><span data-stu-id="25cd4-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="25cd4-109">Bu komut MyResourceGroup adlı kaynak grubundaki MyNetworkInterface adlı ağ arabirimiyle ilişkili etkin yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="25cd4-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="25cd4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25cd4-110">PARAMETERS</span></span>

### <span data-ttu-id="25cd4-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="25cd4-111">-AsJob</span></span>
<span data-ttu-id="25cd4-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="25cd4-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25cd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25cd4-113">-DefaultProfile</span></span>
<span data-ttu-id="25cd4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25cd4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25cd4-115">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="25cd4-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="25cd4-116">Ağ arabiriminin adı belirtildi.</span><span class="sxs-lookup"><span data-stu-id="25cd4-116">Specified the name of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25cd4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25cd4-117">-ResourceGroupName</span></span>
<span data-ttu-id="25cd4-118">Ağ arabiriminin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="25cd4-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25cd4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25cd4-119">CommonParameters</span></span>
<span data-ttu-id="25cd4-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25cd4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25cd4-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25cd4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25cd4-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25cd4-122">INPUTS</span></span>

## <span data-ttu-id="25cd4-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25cd4-123">OUTPUTS</span></span>

### <span data-ttu-id="25cd4-124">Microsoft. Azure. Commands. Network. modeller. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="25cd4-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="25cd4-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25cd4-125">NOTES</span></span>

## <span data-ttu-id="25cd4-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25cd4-126">RELATED LINKS</span></span>

[<span data-ttu-id="25cd4-127">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="25cd4-127">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)

