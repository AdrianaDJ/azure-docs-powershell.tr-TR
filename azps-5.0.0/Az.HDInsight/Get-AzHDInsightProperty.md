---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: e13b90da8e1901faf0b18eb6ebf3cc78ce1bbcda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319566"
---
# <span data-ttu-id="b8fa1-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="b8fa1-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="b8fa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="b8fa1-103">HDInsight hizmeti hakkında, kullanılabilir konumlar ve kapasite gibi özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="b8fa1-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="b8fa1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8fa1-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8fa1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8fa1-105">DESCRIPTION</span></span>
<span data-ttu-id="b8fa1-106">**Get-AzHDInsightProperty** cmdlet 'i, kullanılabilir konumlar, HDInsight küme sürümleri ve kullanılabilir işlem kapasitesi gibi Azure HDInsight 'a özgü özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="b8fa1-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="b8fa1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8fa1-107">EXAMPLES</span></span>

### <span data-ttu-id="b8fa1-108">Örnek 1: Azure HDInsight kümesinin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="b8fa1-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="b8fa1-109">Bu komut, bir HDInsight hizmetinden Doğu US 2 konumundan Özellikler alır.</span><span class="sxs-lookup"><span data-stu-id="b8fa1-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="b8fa1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8fa1-110">PARAMETERS</span></span>

### <span data-ttu-id="b8fa1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8fa1-111">-DefaultProfile</span></span>
<span data-ttu-id="b8fa1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b8fa1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8fa1-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="b8fa1-113">-Location</span></span>
<span data-ttu-id="b8fa1-114">HDInsight özelliklerinin getirileceği konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8fa1-114">Specifies the location for which to fetch HDInsight properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8fa1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8fa1-115">CommonParameters</span></span>
<span data-ttu-id="b8fa1-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8fa1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8fa1-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b8fa1-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8fa1-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8fa1-118">INPUTS</span></span>

### <span data-ttu-id="b8fa1-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b8fa1-119">None</span></span>
## <span data-ttu-id="b8fa1-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8fa1-120">OUTPUTS</span></span>

### <span data-ttu-id="b8fa1-121">Microsoft. Azure. Management. HDInsight. modeller. AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="b8fa1-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="b8fa1-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8fa1-122">NOTES</span></span>

## <span data-ttu-id="b8fa1-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8fa1-123">RELATED LINKS</span></span>
