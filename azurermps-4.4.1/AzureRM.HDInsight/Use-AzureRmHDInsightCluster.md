---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: 01f9a2a9bae03606773c146f44f7e737fb9b613f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764834"
---
# <span data-ttu-id="92f9a-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="92f9a-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="92f9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92f9a-102">SYNOPSIS</span></span>
<span data-ttu-id="92f9a-103">Invoke-RmAzureHDInsightHiveJob cmdlet 'inde kullanılacak kümeyi seçer.</span><span class="sxs-lookup"><span data-stu-id="92f9a-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92f9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92f9a-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92f9a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="92f9a-105">DESCRIPTION</span></span>
<span data-ttu-id="92f9a-106">**Use-AzureRmHDInsightCluster** cmdlet 'i, Invoke-AzureRmHDInsightHiveJob cmdlet 'Inin, kovan işlerini göndermek Için kullanacağı Azure HDInsight kümesini seçer.</span><span class="sxs-lookup"><span data-stu-id="92f9a-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="92f9a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92f9a-107">EXAMPLES</span></span>

### <span data-ttu-id="92f9a-108">Örnek 1: yığın sorgu gönderimi için küme seçme</span><span class="sxs-lookup"><span data-stu-id="92f9a-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="92f9a-109">Bu komut, kovan sorgu gönderimi için bir küme seçer.</span><span class="sxs-lookup"><span data-stu-id="92f9a-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="92f9a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92f9a-110">PARAMETERS</span></span>

### <span data-ttu-id="92f9a-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="92f9a-111">-ClusterName</span></span>
<span data-ttu-id="92f9a-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92f9a-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="92f9a-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="92f9a-113">-HttpCredential</span></span>
<span data-ttu-id="92f9a-114">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92f9a-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f9a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f9a-115">-ResourceGroupName</span></span>
<span data-ttu-id="92f9a-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92f9a-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f9a-117">-DefaultProfile</span></span>
<span data-ttu-id="92f9a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92f9a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92f9a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f9a-119">CommonParameters</span></span>
<span data-ttu-id="92f9a-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92f9a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f9a-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f9a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f9a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92f9a-122">INPUTS</span></span>

## <span data-ttu-id="92f9a-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92f9a-123">OUTPUTS</span></span>

### <span data-ttu-id="92f9a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="92f9a-124">System.String</span></span>

## <span data-ttu-id="92f9a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92f9a-125">NOTES</span></span>

## <span data-ttu-id="92f9a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92f9a-126">RELATED LINKS</span></span>

[<span data-ttu-id="92f9a-127">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="92f9a-127">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="92f9a-128">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="92f9a-128">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


