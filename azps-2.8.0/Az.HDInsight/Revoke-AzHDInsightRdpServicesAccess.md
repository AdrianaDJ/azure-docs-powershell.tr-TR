---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 7f5fcb8dcfbb325b8bc0381b3c943e550fe27e62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751810"
---
# <span data-ttu-id="c8286-101">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c8286-101">Revoke-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="c8286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8286-102">SYNOPSIS</span></span>
<span data-ttu-id="c8286-103">Windows kümesine RDP erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="c8286-103">Disables RDP access to a Windows cluster.</span></span>

## <span data-ttu-id="c8286-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8286-104">SYNTAX</span></span>

```
Revoke-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8286-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8286-105">DESCRIPTION</span></span>
<span data-ttu-id="c8286-106">**Revoke-AzHDInsightRdpServicesAccess** cmdlet 'i Windows tabanlı bir Azure HDInsight kümesine Uzak Masaüstü Protokolü (RDP) erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="c8286-106">The **Revoke-AzHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c8286-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8286-107">EXAMPLES</span></span>

### <span data-ttu-id="c8286-108">Örnek 1: belirtilen kümeye RDP erişimini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="c8286-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="c8286-109">Bu komut,-Hadoop-001 adlı kümeye RDP erişimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="c8286-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="c8286-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8286-110">PARAMETERS</span></span>

### <span data-ttu-id="c8286-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c8286-111">-ClusterName</span></span>
<span data-ttu-id="c8286-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8286-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c8286-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8286-113">-DefaultProfile</span></span>
<span data-ttu-id="c8286-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c8286-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8286-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8286-115">-ResourceGroupName</span></span>
<span data-ttu-id="c8286-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8286-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c8286-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8286-117">CommonParameters</span></span>
<span data-ttu-id="c8286-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8286-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8286-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8286-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8286-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8286-120">INPUTS</span></span>

### <span data-ttu-id="c8286-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c8286-121">None</span></span>

## <span data-ttu-id="c8286-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8286-122">OUTPUTS</span></span>

### <span data-ttu-id="c8286-123">System. void</span><span class="sxs-lookup"><span data-stu-id="c8286-123">System.Void</span></span>

## <span data-ttu-id="c8286-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8286-124">NOTES</span></span>

## <span data-ttu-id="c8286-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8286-125">RELATED LINKS</span></span>

[<span data-ttu-id="c8286-126">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c8286-126">Grant-AzHDInsightRdpServicesAccess</span></span>](./Grant-AzHDInsightRdpServicesAccess.md)


