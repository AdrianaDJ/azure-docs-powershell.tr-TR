---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: ddc269d342a6119187ec578e236a30c928d9ea3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916560"
---
# <span data-ttu-id="6b52f-101">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6b52f-101">Revoke-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="6b52f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b52f-102">SYNOPSIS</span></span>
<span data-ttu-id="6b52f-103">Kümeye HTTP erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="6b52f-103">Disables HTTP access to the cluster.</span></span>

## <span data-ttu-id="6b52f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b52f-104">SYNTAX</span></span>

```
Revoke-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b52f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b52f-105">DESCRIPTION</span></span>
<span data-ttu-id="6b52f-106">**Revoke-AzHDInsightHttpServicesAccess** CMDLET 'i ODBC, ambarı, Oozie ve webHCatalog Web Services Için Azure HDıNSIGHT kümesine http erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="6b52f-106">The **Revoke-AzHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="6b52f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b52f-107">EXAMPLES</span></span>

### <span data-ttu-id="6b52f-108">Örnek 1: kümeye HTTP erişimini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="6b52f-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="6b52f-109">Bu komut,-hadoop_001 adlı kümeye HTTP erişimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="6b52f-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="6b52f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b52f-110">PARAMETERS</span></span>

### <span data-ttu-id="6b52f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6b52f-111">-ClusterName</span></span>
<span data-ttu-id="6b52f-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b52f-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6b52f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b52f-113">-DefaultProfile</span></span>
<span data-ttu-id="6b52f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6b52f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b52f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b52f-115">-ResourceGroupName</span></span>
<span data-ttu-id="6b52f-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b52f-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6b52f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b52f-117">CommonParameters</span></span>
<span data-ttu-id="6b52f-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b52f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b52f-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b52f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b52f-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b52f-120">INPUTS</span></span>

### <span data-ttu-id="6b52f-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6b52f-121">None</span></span>

## <span data-ttu-id="6b52f-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b52f-122">OUTPUTS</span></span>

### <span data-ttu-id="6b52f-123">Microsoft. Azure. Management. HDInsight. model. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="6b52f-123">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="6b52f-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b52f-124">NOTES</span></span>

## <span data-ttu-id="6b52f-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b52f-125">RELATED LINKS</span></span>

[<span data-ttu-id="6b52f-126">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6b52f-126">Grant-AzHDInsightHttpServicesAccess</span></span>](./Grant-AzHDInsightHttpServicesAccess.md)


