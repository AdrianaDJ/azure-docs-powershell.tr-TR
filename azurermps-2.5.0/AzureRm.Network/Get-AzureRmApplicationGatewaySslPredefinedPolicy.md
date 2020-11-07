---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
ms.openlocfilehash: a977de2b4a60f0fc5ae93e175d521d398d40f850
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940090"
---
# <span data-ttu-id="55c30-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="55c30-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="55c30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55c30-102">SYNOPSIS</span></span>
<span data-ttu-id="55c30-103">Uygulama Ağ Geçidi tarafından sağlanan önceden tanımlanmış SSL Ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="55c30-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55c30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55c30-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55c30-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55c30-105">DESCRIPTION</span></span>
<span data-ttu-id="55c30-106">**Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet 'ı uygulama ağ geçidi tarafından sağlanan önceden tanımlanmış SSL ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="55c30-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="55c30-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55c30-107">EXAMPLES</span></span>

### <span data-ttu-id="55c30-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="55c30-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="55c30-109">Bu komut, önceden tanımlanmış tüm SSL ilkelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="55c30-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="55c30-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="55c30-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="55c30-111">Bu komut, AppGwSslPolicy20170401 adında önceden tanımlanmış ilke döndürür.</span><span class="sxs-lookup"><span data-stu-id="55c30-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="55c30-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55c30-112">PARAMETERS</span></span>

### <span data-ttu-id="55c30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c30-113">-DefaultProfile</span></span>
<span data-ttu-id="55c30-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55c30-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55c30-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="55c30-115">-Name</span></span>
<span data-ttu-id="55c30-116">Önceden tanımlanmış SSL ilkesinin adı</span><span class="sxs-lookup"><span data-stu-id="55c30-116">Name of the ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c30-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c30-117">CommonParameters</span></span>
<span data-ttu-id="55c30-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55c30-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c30-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55c30-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c30-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55c30-120">INPUTS</span></span>

### <span data-ttu-id="55c30-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="55c30-121">None</span></span>

## <span data-ttu-id="55c30-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55c30-122">OUTPUTS</span></span>

### <span data-ttu-id="55c30-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="55c30-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="55c30-124">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="55c30-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="55c30-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55c30-125">NOTES</span></span>

## <span data-ttu-id="55c30-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55c30-126">RELATED LINKS</span></span>

