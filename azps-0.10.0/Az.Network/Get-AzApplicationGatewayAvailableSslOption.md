---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayAvailableSslOption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: e0fa27a99a8a2d00819d558b42218b9405a5f039
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935605"
---
# <span data-ttu-id="81561-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="81561-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="81561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81561-102">SYNOPSIS</span></span>
<span data-ttu-id="81561-103">Uygulama ağ geçidi için SSL ilkesi ile ilgili tüm SSL seçeneklerini alır.</span><span class="sxs-lookup"><span data-stu-id="81561-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="81561-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81561-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81561-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="81561-105">DESCRIPTION</span></span>
<span data-ttu-id="81561-106">**Get-AzApplicationGatewayAvailableSslOption** cmdlet 'i SSL ilkesi için kullanılabilir tüm SSL seçeneklerini alır</span><span class="sxs-lookup"><span data-stu-id="81561-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="81561-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81561-107">EXAMPLES</span></span>

### <span data-ttu-id="81561-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="81561-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="81561-109">Bu komut, SSL ilkesi için kullanılabilir tüm SSL seçeneklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="81561-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="81561-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81561-110">PARAMETERS</span></span>

### <span data-ttu-id="81561-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81561-111">-DefaultProfile</span></span>
<span data-ttu-id="81561-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81561-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81561-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81561-113">CommonParameters</span></span>
<span data-ttu-id="81561-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81561-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81561-115">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81561-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81561-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81561-116">INPUTS</span></span>

### <span data-ttu-id="81561-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="81561-117">None</span></span>

## <span data-ttu-id="81561-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81561-118">OUTPUTS</span></span>

### <span data-ttu-id="81561-119">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="81561-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="81561-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81561-120">NOTES</span></span>

## <span data-ttu-id="81561-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81561-121">RELATED LINKS</span></span>

