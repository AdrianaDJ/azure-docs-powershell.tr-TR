---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: 7e9df747becd5e2bd49b865b61f963d1db585e17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751800"
---
# <span data-ttu-id="52af7-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="52af7-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="52af7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52af7-102">SYNOPSIS</span></span>
<span data-ttu-id="52af7-103">Invoke-RmAzureHDInsightHiveJob cmdlet 'inde kullanılacak kümeyi seçer.</span><span class="sxs-lookup"><span data-stu-id="52af7-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="52af7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52af7-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52af7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="52af7-105">DESCRIPTION</span></span>
<span data-ttu-id="52af7-106">**Use-AzHDInsightCluster** cmdlet 'i, Invoke-AzHDInsightHiveJob cmdlet 'Inin, kovan işlerini göndermek Için kullanacağı Azure HDInsight kümesini seçer.</span><span class="sxs-lookup"><span data-stu-id="52af7-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="52af7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52af7-107">EXAMPLES</span></span>

### <span data-ttu-id="52af7-108">Örnek 1: yığın sorgu gönderimi için küme seçme</span><span class="sxs-lookup"><span data-stu-id="52af7-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="52af7-109">Bu komut, kovan sorgu gönderimi için bir küme seçer.</span><span class="sxs-lookup"><span data-stu-id="52af7-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="52af7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52af7-110">PARAMETERS</span></span>

### <span data-ttu-id="52af7-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="52af7-111">-ClusterName</span></span>
<span data-ttu-id="52af7-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52af7-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="52af7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52af7-113">-DefaultProfile</span></span>
<span data-ttu-id="52af7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="52af7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52af7-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="52af7-115">-HttpCredential</span></span>
<span data-ttu-id="52af7-116">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52af7-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="52af7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52af7-117">-ResourceGroupName</span></span>
<span data-ttu-id="52af7-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52af7-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="52af7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52af7-119">CommonParameters</span></span>
<span data-ttu-id="52af7-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52af7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52af7-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52af7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52af7-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52af7-122">INPUTS</span></span>

### <span data-ttu-id="52af7-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="52af7-123">None</span></span>

## <span data-ttu-id="52af7-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52af7-124">OUTPUTS</span></span>

### <span data-ttu-id="52af7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="52af7-125">System.String</span></span>

## <span data-ttu-id="52af7-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52af7-126">NOTES</span></span>

## <span data-ttu-id="52af7-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52af7-127">RELATED LINKS</span></span>

[<span data-ttu-id="52af7-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="52af7-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="52af7-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="52af7-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

