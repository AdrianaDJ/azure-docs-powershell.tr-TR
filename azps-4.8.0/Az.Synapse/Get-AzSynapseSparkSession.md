---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267507"
---
# <span data-ttu-id="8eab2-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="8eab2-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="8eab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eab2-102">SYNOPSIS</span></span>
<span data-ttu-id="8eab2-103">SYNAPSE Analytics Spark oturumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8eab2-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="8eab2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8eab2-104">SYNTAX</span></span>

### <span data-ttu-id="8eab2-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8eab2-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8eab2-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8eab2-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8eab2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8eab2-107">DESCRIPTION</span></span>
<span data-ttu-id="8eab2-108">**Get-AzSynapseSparkSession** cmdlet 'ı bir Azure SYNAPSE Analytics Spark oturumu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8eab2-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="8eab2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8eab2-109">EXAMPLES</span></span>

### <span data-ttu-id="8eab2-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8eab2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="8eab2-111">Bu komut, belirtilen Spark havuzunun altındaki tüm Spark oturumlarını alır.</span><span class="sxs-lookup"><span data-stu-id="8eab2-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="8eab2-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8eab2-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="8eab2-113">Bu komut, belirtilen Livy KIMLIĞIYLE Spark oturumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8eab2-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="8eab2-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="8eab2-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="8eab2-115">Bu komut, belirtilen Spark havuzunun altındaki tüm Spark oturumlarını ardışık düzen aracılığıyla alır.</span><span class="sxs-lookup"><span data-stu-id="8eab2-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="8eab2-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8eab2-116">PARAMETERS</span></span>

### <span data-ttu-id="8eab2-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8eab2-117">-ApplicationId</span></span>
<span data-ttu-id="8eab2-118">Oturumun uygulama tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="8eab2-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="8eab2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eab2-119">-DefaultProfile</span></span>
<span data-ttu-id="8eab2-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8eab2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eab2-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="8eab2-121">-LivyId</span></span>
<span data-ttu-id="8eab2-122">Spark oturumunun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="8eab2-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="8eab2-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="8eab2-123">-Name</span></span>
<span data-ttu-id="8eab2-124">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="8eab2-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="8eab2-125">-Parlak PoolName</span><span class="sxs-lookup"><span data-stu-id="8eab2-125">-SparkPoolName</span></span>
<span data-ttu-id="8eab2-126">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="8eab2-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eab2-127">-Parlak Poolobject</span><span class="sxs-lookup"><span data-stu-id="8eab2-127">-SparkPoolObject</span></span>
<span data-ttu-id="8eab2-128">Genellikle ardışık düzen aracılığıyla geçen Spark havuz giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8eab2-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eab2-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="8eab2-129">-WorkspaceName</span></span>
<span data-ttu-id="8eab2-130">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="8eab2-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eab2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eab2-131">CommonParameters</span></span>
<span data-ttu-id="8eab2-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8eab2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eab2-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8eab2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eab2-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8eab2-134">INPUTS</span></span>

### <span data-ttu-id="8eab2-135">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="8eab2-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="8eab2-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8eab2-136">OUTPUTS</span></span>

### <span data-ttu-id="8eab2-137">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="8eab2-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="8eab2-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8eab2-138">NOTES</span></span>

## <span data-ttu-id="8eab2-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8eab2-139">RELATED LINKS</span></span>
