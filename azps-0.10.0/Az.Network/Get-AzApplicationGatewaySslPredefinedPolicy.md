---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 2c55da6b7193d02de51e273df4626152d6d088fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935567"
---
# <span data-ttu-id="e49b6-101">Get-AzApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="e49b6-101">Get-AzApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="e49b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e49b6-102">SYNOPSIS</span></span>
<span data-ttu-id="e49b6-103">Uygulama Ağ Geçidi tarafından sağlanan önceden tanımlanmış SSL Ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="e49b6-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="e49b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e49b6-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e49b6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e49b6-105">DESCRIPTION</span></span>
<span data-ttu-id="e49b6-106">**Get-AzApplicationGatewaySslPredefinedPolicy** cmdlet 'ı, uygulama ağ geçidi tarafından sağlanan önceden tanımlanmış SSL ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="e49b6-106">The **Get-AzApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="e49b6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e49b6-107">EXAMPLES</span></span>

### <span data-ttu-id="e49b6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e49b6-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="e49b6-109">Bu komut, önceden tanımlanmış tüm SSL ilkelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e49b6-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="e49b6-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e49b6-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="e49b6-111">Bu komut, AppGwSslPolicy20170401 adında önceden tanımlanmış ilke döndürür.</span><span class="sxs-lookup"><span data-stu-id="e49b6-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="e49b6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e49b6-112">PARAMETERS</span></span>

### <span data-ttu-id="e49b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49b6-113">-DefaultProfile</span></span>
<span data-ttu-id="e49b6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e49b6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e49b6-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e49b6-115">-Name</span></span>
<span data-ttu-id="e49b6-116">Önceden tanımlanmış SSL ilkesinin adı</span><span class="sxs-lookup"><span data-stu-id="e49b6-116">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="e49b6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49b6-117">CommonParameters</span></span>
<span data-ttu-id="e49b6-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e49b6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49b6-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e49b6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49b6-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e49b6-120">INPUTS</span></span>

### <span data-ttu-id="e49b6-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e49b6-121">None</span></span>

## <span data-ttu-id="e49b6-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e49b6-122">OUTPUTS</span></span>

### <span data-ttu-id="e49b6-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="e49b6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="e49b6-124">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e49b6-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e49b6-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e49b6-125">NOTES</span></span>

## <span data-ttu-id="e49b6-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e49b6-126">RELATED LINKS</span></span>

