---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278464"
---
# <span data-ttu-id="72fa1-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="72fa1-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="72fa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="72fa1-103">Depolama hesabının yük devretmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="72fa1-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="72fa1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72fa1-104">SYNTAX</span></span>

### <span data-ttu-id="72fa1-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="72fa1-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72fa1-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="72fa1-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72fa1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="72fa1-107">DESCRIPTION</span></span>
<span data-ttu-id="72fa1-108">Depolama hesabının yük devretmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="72fa1-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="72fa1-109">Kullanılabilir durumda bir depolama hesabı için yük devretme isteği tetiklenebilir.</span><span class="sxs-lookup"><span data-stu-id="72fa1-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="72fa1-110">Yük devretme işlemi depolama hesabının birincil kümesinden RA-GRS hesapları için ikincil kümeye yapılır.</span><span class="sxs-lookup"><span data-stu-id="72fa1-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="72fa1-111">İkinci küme, yük devretmeden sonra birincili olacak.</span><span class="sxs-lookup"><span data-stu-id="72fa1-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="72fa1-112">Yük devretmeyi başlatmadan önce lütfen depolama hesabınıza şu etkiyi yapın: 1,1.</span><span class="sxs-lookup"><span data-stu-id="72fa1-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="72fa1-113">Lütfen blob hizmet istatistiklerini al 'ı kullanarak son eşitleme zamanını denetleyin ( https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) , tablo hizmet istatistiklerini alın ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) ve hesap Için sıra HIZMETI istatistiklerini alın ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) hesabınız için.</span><span class="sxs-lookup"><span data-stu-id="72fa1-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="72fa1-114">Bu, yük devretmeyi başlattığınızda kaybedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72fa1-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="72fa1-115">2. yük devretmenin ardından depolama hesabı türünüz yerel olarak yedekli depolama alanına (LRS) dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="72fa1-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="72fa1-116">Hesabınızı coğrafi olarak yedekli depolama (GRS) kullanacak şekilde dönüştürebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72fa1-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="72fa1-117">3. depolama hesabınız için GRS 'i yeniden etkinleştirdiğinizde, Microsoft verileri yeni ikincil bölgenize çoğaltır.</span><span class="sxs-lookup"><span data-stu-id="72fa1-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="72fa1-118">Çoğaltma süresi, çoğaltılacak veri miktarına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="72fa1-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="72fa1-119">Lütfen önyükleme için bant genişliği ücretleri bulunduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="72fa1-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="72fa1-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="72fa1-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="72fa1-121">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72fa1-121">EXAMPLES</span></span>

### <span data-ttu-id="72fa1-122">Örnek 1: depolama hesabının yük devretmesini çağırma</span><span class="sxs-lookup"><span data-stu-id="72fa1-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="72fa1-123">Bu komut depolama hesabının son eşitleme süresini denetleyip, bu işlemi yerine çalışma</span><span class="sxs-lookup"><span data-stu-id="72fa1-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="72fa1-124">Çalışma süresi uzun zamandır, arka uç-Iş parametresiyle çalıştırmayı önerin ve ardından işin tamamlanmasını bekleyin.</span><span class="sxs-lookup"><span data-stu-id="72fa1-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="72fa1-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72fa1-125">PARAMETERS</span></span>

### <span data-ttu-id="72fa1-126">-Iş</span><span class="sxs-lookup"><span data-stu-id="72fa1-126">-AsJob</span></span>
<span data-ttu-id="72fa1-127">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="72fa1-127">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72fa1-128">-DefaultProfile</span></span>
<span data-ttu-id="72fa1-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72fa1-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72fa1-130">-Force</span><span class="sxs-lookup"><span data-stu-id="72fa1-130">-Force</span></span>
<span data-ttu-id="72fa1-131">Hesabı yük devretmeye zorla</span><span class="sxs-lookup"><span data-stu-id="72fa1-131">Force to Failover the Account</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72fa1-132">-InputObject</span></span>
<span data-ttu-id="72fa1-133">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="72fa1-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="72fa1-134">-Name</span></span>
<span data-ttu-id="72fa1-135">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="72fa1-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72fa1-136">-ResourceGroupName</span></span>
<span data-ttu-id="72fa1-137">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="72fa1-137">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="72fa1-138">-Confirm</span></span>
<span data-ttu-id="72fa1-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72fa1-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72fa1-140">-WhatIf</span></span>
<span data-ttu-id="72fa1-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72fa1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72fa1-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72fa1-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fa1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72fa1-143">CommonParameters</span></span>
<span data-ttu-id="72fa1-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72fa1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72fa1-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72fa1-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72fa1-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72fa1-146">INPUTS</span></span>

### <span data-ttu-id="72fa1-147">System. String</span><span class="sxs-lookup"><span data-stu-id="72fa1-147">System.String</span></span>

## <span data-ttu-id="72fa1-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72fa1-148">OUTPUTS</span></span>

### <span data-ttu-id="72fa1-149">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="72fa1-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="72fa1-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72fa1-150">NOTES</span></span>

## <span data-ttu-id="72fa1-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72fa1-151">RELATED LINKS</span></span>
