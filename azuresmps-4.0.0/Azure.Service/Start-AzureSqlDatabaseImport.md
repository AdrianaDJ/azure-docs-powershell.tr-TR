---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105427"
---
# <span data-ttu-id="b4060-101">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="b4060-101">Start-AzureSqlDatabaseImport</span></span>

## <span data-ttu-id="b4060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4060-102">SYNOPSIS</span></span>
<span data-ttu-id="b4060-103">BLOB depolama alanından bir Azure SQL veritabanına içeri aktarma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="b4060-103">Starts an import operation from blob storage to an Azure SQL Database.</span></span>

## <span data-ttu-id="b4060-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4060-104">SYNTAX</span></span>

### <span data-ttu-id="b4060-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="b4060-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b4060-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="b4060-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b4060-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4060-107">DESCRIPTION</span></span>
<span data-ttu-id="b4060-108">**Start-Azuresddatabaseımport** cmdlet 'ı Azure Blob depolamasındaki BIR Azure SQL veritabanına içeri aktarma işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="b4060-108">The **Start-AzureSqlDatabaseImport** cmdlet starts an import operation from Azure Blob storage to an Azure SQL Database.</span></span>
<span data-ttu-id="b4060-109">Veritabanı yoksa, bu cmdlet bunu belirttiğiniz boyut ve sürüm değerlerini kullanarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4060-109">If the database does not exist, this cmdlet creates it by using the size and edition values that you specify.</span></span>
<span data-ttu-id="b4060-110">İşlem bir veritabanı sunucusu bağlantı bağlamı gerektiriyor.</span><span class="sxs-lookup"><span data-stu-id="b4060-110">The operation requires a database server connection context.</span></span>
<span data-ttu-id="b4060-111">İçeri aktarma işleminin durumunu almak için Get-AzureSqlDatabaseImportExportStatus cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b4060-111">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the import operation.</span></span>

## <span data-ttu-id="b4060-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4060-112">EXAMPLES</span></span>

### <span data-ttu-id="b4060-113">Örnek 1: veritabanını Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="b4060-113">Example 1: Import a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="b4060-114">Bu örnek, $BlobName değişkeninde blob depolamasındaki bir içeri aktarma işlemini DatabaseName adlı Azure SQL veritabanına oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4060-114">This example initiates an import process from the Blob storage in the $BlobName variable into the Azure SQL Database named DatabaseName.</span></span>

## <span data-ttu-id="b4060-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4060-115">PARAMETERS</span></span>

### <span data-ttu-id="b4060-116">-BlobName</span><span class="sxs-lookup"><span data-stu-id="b4060-116">-BlobName</span></span>
<span data-ttu-id="b4060-117">Bu cmdlet 'in veritabanını içeri aktardıkları Azure Blob deposunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4060-117">Specifies the name of the Azure Blob storage from which this cmdlet imports the database.</span></span>

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

### <span data-ttu-id="b4060-118">-DatabaseMaxSize</span><span class="sxs-lookup"><span data-stu-id="b4060-118">-DatabaseMaxSize</span></span>
<span data-ttu-id="b4060-119">Veritabanı için en büyük boyutu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4060-119">Specifies the maximum size, in gigabytes, for the database.</span></span>
<span data-ttu-id="b4060-120">Veritabanı yoksa, bu cmdlet bu en büyük boyutu temel alarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4060-120">If the database does not exist, this cmdlet creates it based on this maximum size.</span></span>
<span data-ttu-id="b4060-121">Kabul edilebilir değerler sürüme göre farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4060-121">The acceptable values differ based on edition.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4060-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b4060-122">-DatabaseName</span></span>
<span data-ttu-id="b4060-123">Veritabanı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4060-123">Specifies a name for the database.</span></span>
<span data-ttu-id="b4060-124">Veritabanı yoksa, bu cmdlet bunu oluşturur ve bu parametrenin belirttiği adı atar.</span><span class="sxs-lookup"><span data-stu-id="b4060-124">If the database does not exist, this cmdlet creates it, and assigns the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4060-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="b4060-125">-Edition</span></span>
<span data-ttu-id="b4060-126">Veritabanının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4060-126">Specifies the edition of the database.</span></span>
<span data-ttu-id="b4060-127">Veritabanı yoksa, bu cmdlet bu sürüm olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4060-127">If the database does not exist, this cmdlet creates it as this edition.</span></span>
<span data-ttu-id="b4060-128">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="b4060-128">Valid values are:</span></span> 

- <span data-ttu-id="b4060-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b4060-129">None</span></span>
- <span data-ttu-id="b4060-130">Web</span><span class="sxs-lookup"><span data-stu-id="b4060-130">Web</span></span> 
- <span data-ttu-id="b4060-131">Karar</span><span class="sxs-lookup"><span data-stu-id="b4060-131">Business</span></span> 
- <span data-ttu-id="b4060-132">Ana</span><span class="sxs-lookup"><span data-stu-id="b4060-132">Basic</span></span>
- <span data-ttu-id="b4060-133">Ardından</span><span class="sxs-lookup"><span data-stu-id="b4060-133">Standard</span></span>
- <span data-ttu-id="b4060-134">Min</span><span class="sxs-lookup"><span data-stu-id="b4060-134">Premium</span></span>

<span data-ttu-id="b4060-135">Varsayılan Web.</span><span class="sxs-lookup"><span data-stu-id="b4060-135">The default is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4060-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="b4060-136">-Profile</span></span>
<span data-ttu-id="b4060-137">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4060-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4060-138">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b4060-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4060-139">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="b4060-139">-SqlConnectionContext</span></span>
<span data-ttu-id="b4060-140">Veritabanının bulunduğu sunucunun bağlantı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4060-140">Specifies the connection context of a server that contains the database.</span></span>

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4060-141">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="b4060-141">-StorageContainer</span></span>
<span data-ttu-id="b4060-142">Bu cmdlet 'in bir veritabanını aldığı blob 'U içeren depolama kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4060-142">Specifies the storage container that contains the Blob from which this cmdlet imports a database.</span></span>

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4060-143">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="b4060-143">-StorageContainerName</span></span>
<span data-ttu-id="b4060-144">BLOB depolama kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4060-144">Specifies the name of the Blob storage container.</span></span>

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4060-145">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="b4060-145">-StorageContext</span></span>
<span data-ttu-id="b4060-146">BLOB depolama kapsayıcısı 'nın bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4060-146">Specifies the context of the Blob storage container.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4060-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4060-147">CommonParameters</span></span>
<span data-ttu-id="b4060-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4060-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4060-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4060-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4060-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4060-150">INPUTS</span></span>

## <span data-ttu-id="b4060-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4060-151">OUTPUTS</span></span>

### <span data-ttu-id="b4060-152">Microsoft. Windowsazde. Commands. SqlDatabase. Services. ımportexportrequest</span><span class="sxs-lookup"><span data-stu-id="b4060-152">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="b4060-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4060-153">NOTES</span></span>

## <span data-ttu-id="b4060-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4060-154">RELATED LINKS</span></span>

[<span data-ttu-id="b4060-155">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="b4060-155">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="b4060-156">Veritabanını içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="b4060-156">Import Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[<span data-ttu-id="b4060-157">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="b4060-157">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="b4060-158">Get-Azuressqldatabaseımportexportstatus</span><span class="sxs-lookup"><span data-stu-id="b4060-158">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="b4060-159">Start-Azuressqldatabaseexport</span><span class="sxs-lookup"><span data-stu-id="b4060-159">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)


