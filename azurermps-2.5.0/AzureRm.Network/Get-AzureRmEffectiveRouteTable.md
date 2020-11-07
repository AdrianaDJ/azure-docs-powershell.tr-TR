---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
ms.openlocfilehash: 403a3d37418e022032988d5d7fccb40a1e79f449
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939131"
---
# <span data-ttu-id="2c2db-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="2c2db-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="2c2db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c2db-102">SYNOPSIS</span></span>
<span data-ttu-id="2c2db-103">Ağ arabiriminin etkin yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="2c2db-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c2db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c2db-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c2db-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c2db-105">DESCRIPTION</span></span>
<span data-ttu-id="2c2db-106">**Get-AzureRmEffectiveRouteTable** cmdlet 'i, bir ağ arabirimine uygulanan etkin yol tablosunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="2c2db-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="2c2db-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c2db-107">EXAMPLES</span></span>

### <span data-ttu-id="2c2db-108">Örnek 1: ağ arabiriminde etkin yol tablosunu alma</span><span class="sxs-lookup"><span data-stu-id="2c2db-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2c2db-109">Bu komut MyResourceGroup adlı kaynak grubundaki MyNetworkInterface adlı ağ arabirimiyle ilişkili etkin yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="2c2db-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2c2db-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c2db-110">PARAMETERS</span></span>

### <span data-ttu-id="2c2db-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="2c2db-111">-AsJob</span></span>
<span data-ttu-id="2c2db-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2c2db-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c2db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c2db-113">-DefaultProfile</span></span>
<span data-ttu-id="2c2db-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c2db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c2db-115">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="2c2db-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="2c2db-116">Ağ arabiriminin adı belirtildi.</span><span class="sxs-lookup"><span data-stu-id="2c2db-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="2c2db-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c2db-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c2db-118">Ağ arabiriminin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c2db-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="2c2db-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c2db-119">CommonParameters</span></span>
<span data-ttu-id="2c2db-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c2db-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c2db-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c2db-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c2db-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c2db-122">INPUTS</span></span>

## <span data-ttu-id="2c2db-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c2db-123">OUTPUTS</span></span>

### <span data-ttu-id="2c2db-124">Microsoft. Azure. Commands. Network. modeller. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="2c2db-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="2c2db-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c2db-125">NOTES</span></span>

## <span data-ttu-id="2c2db-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c2db-126">RELATED LINKS</span></span>

[<span data-ttu-id="2c2db-127">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2c2db-127">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


