---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105423"
---
# <span data-ttu-id="fcd0c-101">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="fcd0c-101">Start-AzureSqlDatabaseRecovery</span></span>

## <span data-ttu-id="fcd0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcd0c-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd0c-103">Veritabanı için geri yükleme isteği başlatır.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-103">Initiates a restore request for a database.</span></span>

## <span data-ttu-id="fcd0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fcd0c-104">SYNTAX</span></span>

### <span data-ttu-id="fcd0c-105">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fcd0c-105">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fcd0c-106">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fcd0c-106">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fcd0c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fcd0c-107">DESCRIPTION</span></span>
<span data-ttu-id="fcd0c-108">**Start-AzureSqlDatabaseRecovery** cmdlet 'i canlı veya bırakılmış bir veritabanı için geri yükleme isteği başlatır.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-108">The **Start-AzureSqlDatabaseRecovery** cmdlet initiates a restore request for a live or dropped database.</span></span>
<span data-ttu-id="fcd0c-109">Bu cmdlet, veritabanında bilinen son kullanılabilir yedeği kullanan temel kurtarmayı destekler.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-109">This cmdlet supports basic recovery that uses the last known available backup for the database.</span></span>
<span data-ttu-id="fcd0c-110">Kurtarma işlemi yeni bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-110">The recovery operation creates a new database.</span></span>
<span data-ttu-id="fcd0c-111">Bir Live veritabanını aynı sunucuda kurtarmanız durumunda, yeni veritabanı için farklı bir ad belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-111">If you recover a live database on the same server, you must specify a different name for the new database.</span></span>

<span data-ttu-id="fcd0c-112">Bir veritabanı için zaman içinde bir nokta geri yükleme yapmak istiyorsanız, bunun yerine **Start-AzureSqlDatabaseRestore** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-112">To do a point in time restore for a database, use the **Start-AzureSqlDatabaseRestore** cmdlet instead.</span></span>

## <span data-ttu-id="fcd0c-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fcd0c-113">EXAMPLES</span></span>

### <span data-ttu-id="fcd0c-114">Örnek 1: nesne olarak belirtilen veritabanını kurtarma</span><span class="sxs-lookup"><span data-stu-id="fcd0c-114">Example 1: Recover a database specified as an object</span></span>
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="fcd0c-115">İlk komut **Get-Azuresılrecoverrecoverabledatabase** cmdlet 'ini kullanarak bir veritabanı nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-115">The first command gets a database object by using the **Get-AzureSqlRecoverableDatabase** cmdlet.</span></span>
<span data-ttu-id="fcd0c-116">Komut bu nesneyi $Database değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-116">The command stores that object in the $Database variable.</span></span>

<span data-ttu-id="fcd0c-117">İkinci komut $Database depolanan veritabanını kurtarır.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-117">The second command recovers the database stored in $Database.</span></span>

### <span data-ttu-id="fcd0c-118">Örnek 2: adla belirtilen bir veritabanını kurtarma</span><span class="sxs-lookup"><span data-stu-id="fcd0c-118">Example 2: Recover a database specified by name</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="fcd0c-119">Bu komut, veritabanı adını kullanarak veritabanını kurtarır.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-119">This command recovers a database using the database name.</span></span>

## <span data-ttu-id="fcd0c-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fcd0c-120">PARAMETERS</span></span>

### <span data-ttu-id="fcd0c-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="fcd0c-121">-Profile</span></span>
<span data-ttu-id="fcd0c-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fcd0c-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fcd0c-124">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="fcd0c-124">-SourceDatabase</span></span>
<span data-ttu-id="fcd0c-125">Bu cmdlet 'in kurtarakullandığı veritabanını temsil eden veritabanı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-125">Specifies the database object that represents the database that this cmdlet recovers.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd0c-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fcd0c-126">-SourceDatabaseName</span></span>
<span data-ttu-id="fcd0c-127">Bu cmdlet 'in kurtarakullandığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-127">Specifies the name of the database that this cmdlet recovers.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd0c-128">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="fcd0c-128">-SourceServerName</span></span>
<span data-ttu-id="fcd0c-129">Kaynak veritabanının canlı ve çalışıyor olduğu veya kaynak veritabanının silinmeden önce çalıştığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-129">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd0c-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fcd0c-130">-TargetDatabaseName</span></span>
<span data-ttu-id="fcd0c-131">Kurtarılan veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-131">Specifies the name of the recovered database.</span></span>
<span data-ttu-id="fcd0c-132">Kaynak veritabanı hala canlı durumdaysa, aynı sunucuya kurtarmak için kaynak veritabanı adından farklı bir ad belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-132">If the source database is still live, in order to recover it to the same server, you must specify a name that differs from the source database name.</span></span>

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

### <span data-ttu-id="fcd0c-133">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="fcd0c-133">-TargetServerName</span></span>
<span data-ttu-id="fcd0c-134">Veritabanının geri yükleneceği sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-134">Specifies the name of the server to which to restore a database.</span></span>
<span data-ttu-id="fcd0c-135">Bir veritabanını aynı sunucuya veya farklı bir sunucuya geri yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-135">You can restore a database to the same server or to a different server.</span></span>

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

### <span data-ttu-id="fcd0c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd0c-136">CommonParameters</span></span>
<span data-ttu-id="fcd0c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd0c-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcd0c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd0c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fcd0c-139">INPUTS</span></span>

### <span data-ttu-id="fcd0c-140">Microsoft. Windowsazme. Management. Sql. modeller. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="fcd0c-140">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="fcd0c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fcd0c-141">OUTPUTS</span></span>

### <span data-ttu-id="fcd0c-142">Microsoft. Windowsazve. Management. Sql. modeller. RecoverDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="fcd0c-142">Microsoft.WindowsAzure.Management.Sql.Models.RecoverDatabaseOperation</span></span>

## <span data-ttu-id="fcd0c-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fcd0c-143">NOTES</span></span>
* <span data-ttu-id="fcd0c-144">Bu cmdlet 'i çalıştırmak için sertifika tabanlı kimlik doğrulaması kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="fcd0c-144">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="fcd0c-145">Bu cmdlet 'i çalıştırdığınız bilgisayarda aşağıdaki komutları çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="fcd0c-145">Run the following commands on the computer where you run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="fcd0c-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fcd0c-146">RELATED LINKS</span></span>

[<span data-ttu-id="fcd0c-147">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="fcd0c-147">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="fcd0c-148">Veritabanı kurtarma Isteği oluşturma</span><span class="sxs-lookup"><span data-stu-id="fcd0c-148">Create Database Recovery Request</span></span>](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[<span data-ttu-id="fcd0c-149">Azure SQL veritabanında coğrafi çoğaltma</span><span class="sxs-lookup"><span data-stu-id="fcd0c-149">Geo-Replication in Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[<span data-ttu-id="fcd0c-150">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="fcd0c-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="fcd0c-151">Get-Azuressqlrecoverabledatabase</span><span class="sxs-lookup"><span data-stu-id="fcd0c-151">Get-AzureSqlRecoverableDatabase</span></span>](./Get-AzureSqlRecoverableDatabase.md)

[<span data-ttu-id="fcd0c-152">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="fcd0c-152">Start-AzureSqlDatabaseRestore</span></span>](./Start-AzureSqlDatabaseRestore.md)


