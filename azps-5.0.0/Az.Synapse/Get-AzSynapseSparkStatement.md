---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324151"
---
# <span data-ttu-id="7e05d-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="7e05d-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="7e05d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e05d-102">SYNOPSIS</span></span>
<span data-ttu-id="7e05d-103">SYNAPSE analitik Spark deyimini alır.</span><span class="sxs-lookup"><span data-stu-id="7e05d-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="7e05d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e05d-104">SYNTAX</span></span>

### <span data-ttu-id="7e05d-105">Getkenstatestatesbyıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7e05d-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e05d-106">Getmini Ifade. Sbyparentobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="7e05d-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e05d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e05d-107">DESCRIPTION</span></span>
<span data-ttu-id="7e05d-108">**Get-AzSynapseSparkStatement** cmdlet 'ı bir Azure SYNAPSE Analytics Spark deyimiyle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="7e05d-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="7e05d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e05d-109">EXAMPLES</span></span>

### <span data-ttu-id="7e05d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7e05d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="7e05d-111">Bu komut, bir Spark oturumunun altındaki tüm Spark deyimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="7e05d-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="7e05d-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7e05d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="7e05d-113">Bu komut, belirtilen Livy KIMLIĞINE sahip Spark deyimini alır.</span><span class="sxs-lookup"><span data-stu-id="7e05d-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="7e05d-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="7e05d-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="7e05d-115">Bu komut, ardışık düzen aracılığıyla Spark oturumunun altındaki tüm Spark deyimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="7e05d-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="7e05d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e05d-116">PARAMETERS</span></span>

### <span data-ttu-id="7e05d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e05d-117">-DefaultProfile</span></span>
<span data-ttu-id="7e05d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e05d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e05d-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="7e05d-119">-LivyId</span></span>
<span data-ttu-id="7e05d-120">Spark deyiminin tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="7e05d-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e05d-121">-SessionID</span><span class="sxs-lookup"><span data-stu-id="7e05d-121">-SessionId</span></span>
<span data-ttu-id="7e05d-122">Spark oturumunun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="7e05d-122">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e05d-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="7e05d-123">-SessionObject</span></span>
<span data-ttu-id="7e05d-124">Genellikle ardışık düzen aracılığıyla geçen Spark havuz giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7e05d-124">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e05d-125">-Parlak PoolName</span><span class="sxs-lookup"><span data-stu-id="7e05d-125">-SparkPoolName</span></span>
<span data-ttu-id="7e05d-126">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="7e05d-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e05d-127">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="7e05d-127">-WorkspaceName</span></span>
<span data-ttu-id="7e05d-128">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="7e05d-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e05d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e05d-129">CommonParameters</span></span>
<span data-ttu-id="7e05d-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e05d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e05d-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7e05d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e05d-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e05d-132">INPUTS</span></span>

### <span data-ttu-id="7e05d-133">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="7e05d-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="7e05d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e05d-134">OUTPUTS</span></span>

### <span data-ttu-id="7e05d-135">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="7e05d-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="7e05d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e05d-136">NOTES</span></span>

## <span data-ttu-id="7e05d-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e05d-137">RELATED LINKS</span></span>
