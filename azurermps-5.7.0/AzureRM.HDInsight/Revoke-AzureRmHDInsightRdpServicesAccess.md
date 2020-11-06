---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 32664beb1ffe7600756953294b1ec33f7d1d54ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592502"
---
# <span data-ttu-id="61114-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="61114-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="61114-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61114-102">SYNOPSIS</span></span>
<span data-ttu-id="61114-103">Windows kümesine RDP erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="61114-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61114-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61114-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61114-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61114-105">DESCRIPTION</span></span>
<span data-ttu-id="61114-106">**Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet 'i Windows tabanlı bir Azure HDInsight kümesine Uzak Masaüstü Protokolü (RDP) erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="61114-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="61114-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61114-107">EXAMPLES</span></span>

### <span data-ttu-id="61114-108">Örnek 1: belirtilen kümeye RDP erişimini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="61114-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="61114-109">Bu komut,-Hadoop-001 adlı kümeye RDP erişimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="61114-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="61114-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61114-110">PARAMETERS</span></span>

### <span data-ttu-id="61114-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="61114-111">-ClusterName</span></span>
<span data-ttu-id="61114-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61114-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="61114-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61114-113">-DefaultProfile</span></span>
<span data-ttu-id="61114-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="61114-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61114-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61114-115">-ResourceGroupName</span></span>
<span data-ttu-id="61114-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61114-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="61114-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61114-117">CommonParameters</span></span>
<span data-ttu-id="61114-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61114-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61114-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61114-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61114-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61114-120">INPUTS</span></span>

### <span data-ttu-id="61114-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="61114-121">None</span></span>
<span data-ttu-id="61114-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="61114-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61114-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61114-123">OUTPUTS</span></span>

### <span data-ttu-id="61114-124">System. void</span><span class="sxs-lookup"><span data-stu-id="61114-124">System.Void</span></span>

## <span data-ttu-id="61114-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61114-125">NOTES</span></span>

## <span data-ttu-id="61114-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61114-126">RELATED LINKS</span></span>

[<span data-ttu-id="61114-127">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="61114-127">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)


