---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: f42e378bb0bb5202f9f955dea1b844e343a0e037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591111"
---
# <span data-ttu-id="d8495-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d8495-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="d8495-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8495-102">SYNOPSIS</span></span>
<span data-ttu-id="d8495-103">Ağ arabiriminin etkin yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="d8495-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8495-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8495-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8495-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8495-105">DESCRIPTION</span></span>
<span data-ttu-id="d8495-106">**Get-AzureRmEffectiveRouteTable** cmdlet 'i, bir ağ arabirimine uygulanan etkin yol tablosunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="d8495-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="d8495-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8495-107">EXAMPLES</span></span>

### <span data-ttu-id="d8495-108">Örnek 1: ağ arabiriminde etkin yol tablosunu alma</span><span class="sxs-lookup"><span data-stu-id="d8495-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d8495-109">Bu komut MyResourceGroup adlı kaynak grubundaki MyNetworkInterface adlı ağ arabirimiyle ilişkili etkin yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="d8495-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="d8495-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8495-110">PARAMETERS</span></span>

### <span data-ttu-id="d8495-111">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="d8495-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="d8495-112">Ağ arabiriminin adı belirtildi.</span><span class="sxs-lookup"><span data-stu-id="d8495-112">Specified the name of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8495-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8495-113">-ResourceGroupName</span></span>
<span data-ttu-id="d8495-114">Ağ arabiriminin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8495-114">Specifies the resource group of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8495-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8495-115">-DefaultProfile</span></span>
<span data-ttu-id="d8495-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8495-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8495-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8495-117">CommonParameters</span></span>
<span data-ttu-id="d8495-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8495-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8495-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8495-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8495-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8495-120">INPUTS</span></span>

## <span data-ttu-id="d8495-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8495-121">OUTPUTS</span></span>

### <span data-ttu-id="d8495-122">Microsoft. Azure. Commands. Network. modeller. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="d8495-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="d8495-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8495-123">NOTES</span></span>

## <span data-ttu-id="d8495-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8495-124">RELATED LINKS</span></span>

[<span data-ttu-id="d8495-125">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d8495-125">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


