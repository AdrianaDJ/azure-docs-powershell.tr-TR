---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
ms.openlocfilehash: 4b3437f9df1be7e458aaa528769de406d755a071
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592504"
---
# <span data-ttu-id="10159-101">Get-AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="10159-101">Get-AzureRmHDInsightProperties</span></span>

## <span data-ttu-id="10159-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10159-102">SYNOPSIS</span></span>
<span data-ttu-id="10159-103">HDInsight hizmeti hakkında, kullanılabilir konumlar ve kapasite gibi özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="10159-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10159-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10159-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightProperties [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10159-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="10159-105">DESCRIPTION</span></span>
<span data-ttu-id="10159-106">**Get-AzureRmHDInsightProperties** cmdlet 'i, kullanılabilir konumlar, HDInsight küme sürümleri ve kullanılabilir işlem kapasitesi gibi Azure HDInsight 'a özgü özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="10159-106">The **Get-AzureRmHDInsightProperties** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="10159-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10159-107">EXAMPLES</span></span>

### <span data-ttu-id="10159-108">Örnek 1: Azure HDInsight kümesinin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="10159-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightProperties -Location "East US 2"
```

<span data-ttu-id="10159-109">Bu komut, bir HDInsight hizmetinden Doğu US 2 konumundan Özellikler alır.</span><span class="sxs-lookup"><span data-stu-id="10159-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="10159-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10159-110">PARAMETERS</span></span>

### <span data-ttu-id="10159-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10159-111">-DefaultProfile</span></span>
<span data-ttu-id="10159-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="10159-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10159-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="10159-113">-Location</span></span>
<span data-ttu-id="10159-114">HDInsight özelliklerinin getirileceği konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="10159-114">Specifies the location for which to fetch HDInsight properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10159-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10159-115">CommonParameters</span></span>
<span data-ttu-id="10159-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10159-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10159-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10159-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10159-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10159-118">INPUTS</span></span>

### <span data-ttu-id="10159-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="10159-119">None</span></span>
<span data-ttu-id="10159-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="10159-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10159-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10159-121">OUTPUTS</span></span>

### <span data-ttu-id="10159-122">Microsoft. Azure. Management. HDInsight. model. CapabilitiesResponse</span><span class="sxs-lookup"><span data-stu-id="10159-122">Microsoft.Azure.Management.HDInsight.Models.CapabilitiesResponse</span></span>

## <span data-ttu-id="10159-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10159-123">NOTES</span></span>

## <span data-ttu-id="10159-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10159-124">RELATED LINKS</span></span>

