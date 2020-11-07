---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: 7826dad8b9f19e3fc289ec4b08efa98b8b1ed8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763016"
---
# <span data-ttu-id="cfe62-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="cfe62-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="cfe62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfe62-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe62-103">Ağ arabiriminin etkin yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="cfe62-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfe62-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cfe62-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfe62-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cfe62-105">DESCRIPTION</span></span>
<span data-ttu-id="cfe62-106">**Get-AzureRmEffectiveRouteTable** cmdlet 'i, bir ağ arabirimine uygulanan etkin yol tablosunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="cfe62-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="cfe62-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cfe62-107">EXAMPLES</span></span>

### <span data-ttu-id="cfe62-108">Örnek 1: ağ arabiriminde etkin yol tablosunu alma</span><span class="sxs-lookup"><span data-stu-id="cfe62-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="cfe62-109">Bu komut MyResourceGroup adlı kaynak grubundaki MyNetworkInterface adlı ağ arabirimiyle ilişkili etkin yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="cfe62-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="cfe62-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cfe62-110">PARAMETERS</span></span>

### <span data-ttu-id="cfe62-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="cfe62-111">-AsJob</span></span>
<span data-ttu-id="cfe62-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cfe62-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfe62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe62-113">-DefaultProfile</span></span>
<span data-ttu-id="cfe62-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cfe62-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfe62-115">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="cfe62-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="cfe62-116">Ağ arabiriminin adı belirtildi.</span><span class="sxs-lookup"><span data-stu-id="cfe62-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="cfe62-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfe62-117">-ResourceGroupName</span></span>
<span data-ttu-id="cfe62-118">Ağ arabiriminin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe62-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="cfe62-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe62-119">CommonParameters</span></span>
<span data-ttu-id="cfe62-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cfe62-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe62-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfe62-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe62-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cfe62-122">INPUTS</span></span>

### <span data-ttu-id="cfe62-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cfe62-123">None</span></span>
<span data-ttu-id="cfe62-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="cfe62-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cfe62-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cfe62-125">OUTPUTS</span></span>

### <span data-ttu-id="cfe62-126">Microsoft. Azure. Commands. Network. modeller. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="cfe62-126">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="cfe62-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cfe62-127">NOTES</span></span>

## <span data-ttu-id="cfe62-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cfe62-128">RELATED LINKS</span></span>

[<span data-ttu-id="cfe62-129">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cfe62-129">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


