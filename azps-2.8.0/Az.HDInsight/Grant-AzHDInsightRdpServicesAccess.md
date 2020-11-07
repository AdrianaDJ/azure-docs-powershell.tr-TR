---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 6cbe18311f4a14b31bc50f7c0b95266bf99d4a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751839"
---
# <span data-ttu-id="6f562-101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6f562-101">Grant-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="6f562-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f562-102">SYNOPSIS</span></span>
<span data-ttu-id="6f562-103">Windows kümesine RDP erişimi verir.</span><span class="sxs-lookup"><span data-stu-id="6f562-103">Grants RDP access to the Windows cluster.</span></span>

## <span data-ttu-id="6f562-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f562-104">SYNTAX</span></span>

```
Grant-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f562-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f562-105">DESCRIPTION</span></span>
<span data-ttu-id="6f562-106">**Grant-AzHDInsightRdpServicesAccess** cmdlet 'ı, Uzak Masaüstü Protokolü 'NÜN (RDP) Windows tabanlı bir Azure HDInsight kümesine erişmesini olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="6f562-106">The **Grant-AzHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6f562-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f562-107">EXAMPLES</span></span>

### <span data-ttu-id="6f562-108">Örnek 1: Azure HDInsight kümesine RDP erişimi verme</span><span class="sxs-lookup"><span data-stu-id="6f562-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="6f562-109">Bu komut,-Hadoop-001 adlı kümeye RDP erişimi verir.</span><span class="sxs-lookup"><span data-stu-id="6f562-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="6f562-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f562-110">PARAMETERS</span></span>

### <span data-ttu-id="6f562-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6f562-111">-ClusterName</span></span>
<span data-ttu-id="6f562-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f562-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6f562-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f562-113">-DefaultProfile</span></span>
<span data-ttu-id="6f562-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6f562-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f562-115">-Rdpaccessexpme</span><span class="sxs-lookup"><span data-stu-id="6f562-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="6f562-116">Bir kümeye RDP erişimi için **Tarih saat** sonu</span><span class="sxs-lookup"><span data-stu-id="6f562-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f562-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="6f562-117">-RdpCredential</span></span>
<span data-ttu-id="6f562-118">Kümenin RDP kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f562-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="6f562-119">Bu yalnızca Windows kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="6f562-119">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f562-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f562-120">-ResourceGroupName</span></span>
<span data-ttu-id="6f562-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f562-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6f562-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f562-122">CommonParameters</span></span>
<span data-ttu-id="6f562-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f562-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f562-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f562-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f562-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f562-125">INPUTS</span></span>

### <span data-ttu-id="6f562-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6f562-126">None</span></span>

## <span data-ttu-id="6f562-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f562-127">OUTPUTS</span></span>

### <span data-ttu-id="6f562-128">System. void</span><span class="sxs-lookup"><span data-stu-id="6f562-128">System.Void</span></span>

## <span data-ttu-id="6f562-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f562-129">NOTES</span></span>

## <span data-ttu-id="6f562-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f562-130">RELATED LINKS</span></span>

[<span data-ttu-id="6f562-131">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6f562-131">Revoke-AzHDInsightRdpServicesAccess</span></span>](./Revoke-AzHDInsightRdpServicesAccess.md)


