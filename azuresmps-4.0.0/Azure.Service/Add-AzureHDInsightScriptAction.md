---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105720"
---
# <span data-ttu-id="b0a18-101">Add-AzureHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="b0a18-101">Add-AzureHDInsightScriptAction</span></span>

## <span data-ttu-id="b0a18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0a18-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a18-103">HDInsight betik eylemi ekler.</span><span class="sxs-lookup"><span data-stu-id="b0a18-103">Adds an HDInsight script action.</span></span>

## <span data-ttu-id="b0a18-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0a18-104">SYNTAX</span></span>

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0a18-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0a18-105">DESCRIPTION</span></span>
<span data-ttu-id="b0a18-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="b0a18-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="b0a18-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="b0a18-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="b0a18-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="b0a18-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="b0a18-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="b0a18-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="b0a18-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="b0a18-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="b0a18-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b0a18-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="b0a18-112">**Add-AzureHDInsightScriptAction** cmdlet 'i, ek yazılım yüklemek veya Windows PowerShell komut dosyalarını kullanarak bir Hadoop kümesinde çalışan uygulamaların yapılandırmalarını değiştirmek Için kullanılan Azure HDInsight işlevselliğini sağlar.</span><span class="sxs-lookup"><span data-stu-id="b0a18-112">The **Add-AzureHDInsightScriptAction** cmdlet provides Azure HDInsight functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell scripts.</span></span>

<span data-ttu-id="b0a18-113">Bir betik eylemi, HDInsight kümeleri dağıtıldığında küme düğümlerinde çalışır ve kümenin tamamlanma HDInsight yapılandırmasındaki düğümlerden sonra çalışırlar.</span><span class="sxs-lookup"><span data-stu-id="b0a18-113">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="b0a18-114">Komut dosyası eylemi sistem yöneticisi hesap ayrıcalıklarıyla çalışır ve küme düğümlerine tam erişim hakları sağlar.</span><span class="sxs-lookup"><span data-stu-id="b0a18-114">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="b0a18-115">Belirli bir sırada çalışacak bir komut dosyası eylemleri listesi içeren her kümeyi sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0a18-115">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="b0a18-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0a18-116">EXAMPLES</span></span>

### <span data-ttu-id="b0a18-117">Örnek 1: kümeye komut dosyası eylemi ekleme</span><span class="sxs-lookup"><span data-stu-id="b0a18-117">Example 1: Add a script action to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="b0a18-118">İlk komut, bir HDInsight küme yapılandırması oluşturmak için **New-AzureHDInsightClusterConfig** cmdlet 'ini kullanır ve ardından $config değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b0a18-118">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="b0a18-119">İkinci komut, $Config öğesine TestScriptAction adlı betik eylemini eklemek için **Add-AzureHDInsightScriptAction** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b0a18-119">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the script action named TestScriptAction to $Config.</span></span>

<span data-ttu-id="b0a18-120">Son komutu, $Config uygulamasında depolanan komut dosyası eylemini çalıştıran yeni bir HDInsight kümesi oluşturmak için **New-AzureHDInsightCluster** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b0a18-120">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster that runs the script action stored in $Config.</span></span>

### <span data-ttu-id="b0a18-121">Örnek 2: kümeye birden çok betik eylemi ekleme</span><span class="sxs-lookup"><span data-stu-id="b0a18-121">Example 2: Add multiple script actions to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="b0a18-122">İlk komut, bir HDInsight küme yapılandırması oluşturmak için **New-AzureHDInsightClusterConfig** cmdlet 'ini kullanır ve ardından $config değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b0a18-122">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="b0a18-123">İkinci komut, **Add-AzureHDInsightScriptAction** cmdlet 'ini kullanarak belirtilen komut dosyası eylemini $config ve ardından $config **geçirmek için $config ikinci bir komut** dosyası eylemi ekleme</span><span class="sxs-lookup"><span data-stu-id="b0a18-123">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the specified script action to $Config, and then uses the pipeline operator to pass $Config to **Add-AzureHDInsightScriptAction** a second time to add a second script action to $Config.</span></span>

<span data-ttu-id="b0a18-124">Final komutu, $Config komut dosyası eylemlerini çalıştıran bir küme oluşturmak için **New-AzureHDInsightCluster** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b0a18-124">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a cluster that runs the script actions in $Config.</span></span>

## <span data-ttu-id="b0a18-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0a18-125">PARAMETERS</span></span>

### <span data-ttu-id="b0a18-126">-ClusterRoleCollection</span><span class="sxs-lookup"><span data-stu-id="b0a18-126">-ClusterRoleCollection</span></span>
<span data-ttu-id="b0a18-127">Komut dosyası çalıştıracak düğümleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0a18-127">Specifies the nodes for which to run a script.</span></span>
<span data-ttu-id="b0a18-128">Bu parametre için kabul edilebilir değerler: HeadNode veya DataNode.</span><span class="sxs-lookup"><span data-stu-id="b0a18-128">The acceptable values for this parameter are: HeadNode or DataNode.</span></span>

<span data-ttu-id="b0a18-129">Bir değer veya her iki değeri de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0a18-129">You can specify one value or both values.</span></span>

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a18-130">-Config</span><span class="sxs-lookup"><span data-stu-id="b0a18-130">-Config</span></span>
<span data-ttu-id="b0a18-131">Yapılandırma nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0a18-131">Specifies a configuration object.</span></span>
<span data-ttu-id="b0a18-132">Bu cmdlet, bu parametrenin belirttiği nesneye betik eylem bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="b0a18-132">This cmdlet adds script action information to the object that this parameter specifies.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a18-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="b0a18-133">-Name</span></span>
<span data-ttu-id="b0a18-134">Betik eyleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0a18-134">Specifies the name of a script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a18-135">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="b0a18-135">-Parameters</span></span>
<span data-ttu-id="b0a18-136">Komut dosyası eyleminin gerektirdiği parametreleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0a18-136">Specifies the parameters that are required by a script action.</span></span>

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

### <span data-ttu-id="b0a18-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="b0a18-137">-Profile</span></span>
<span data-ttu-id="b0a18-138">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0a18-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b0a18-139">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b0a18-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a18-140">-URI</span><span class="sxs-lookup"><span data-stu-id="b0a18-140">-Uri</span></span>
<span data-ttu-id="b0a18-141">Çalıştırılacak komut dosyasının URI konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0a18-141">Specifies the URI location of a script to run.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a18-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a18-142">CommonParameters</span></span>
<span data-ttu-id="b0a18-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0a18-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a18-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0a18-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a18-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0a18-145">INPUTS</span></span>

## <span data-ttu-id="b0a18-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0a18-146">OUTPUTS</span></span>

## <span data-ttu-id="b0a18-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0a18-147">NOTES</span></span>

## <span data-ttu-id="b0a18-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0a18-148">RELATED LINKS</span></span>

[<span data-ttu-id="b0a18-149">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b0a18-149">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="b0a18-150">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="b0a18-150">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


