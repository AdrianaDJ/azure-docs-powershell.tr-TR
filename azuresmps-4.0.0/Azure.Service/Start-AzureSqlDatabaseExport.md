---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 3005E411-9466-4602-8E07-F4EF8804AB2A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22bff485bf49e0ec5f482e1325af661862583605
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105752"
---
# <span data-ttu-id="b055a-101">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="b055a-101">Start-AzureSqlDatabaseExport</span></span>

## <span data-ttu-id="b055a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b055a-102">SYNOPSIS</span></span>
<span data-ttu-id="b055a-103">Azure SQL veritabanından BLOB depolama birimine dışarı aktarma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="b055a-103">Starts an export operation from an Azure SQL Database to Blob storage.</span></span>

## <span data-ttu-id="b055a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b055a-104">SYNTAX</span></span>

### <span data-ttu-id="b055a-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="b055a-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b055a-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="b055a-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b055a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b055a-107">DESCRIPTION</span></span>
<span data-ttu-id="b055a-108">**Start-azures, databaseexport** cmdlet 'ı Azure SQL veritabanından BLOB depolama birimine dışarı aktarma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="b055a-108">The **Start-AzureSqlDatabaseExport** cmdlet starts an export operation from an Azure SQL Database to Blob storage.</span></span>
<span data-ttu-id="b055a-109">İşlem bir veritabanı sunucusu bağlantı bağlamı gerektiriyor.</span><span class="sxs-lookup"><span data-stu-id="b055a-109">The operation requires a database server connection context.</span></span>
<span data-ttu-id="b055a-110">Dışarı aktarma işleminin durumunu almak için Get-AzureSqlDatabaseImportExportStatus cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b055a-110">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the export operation.</span></span>

## <span data-ttu-id="b055a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b055a-111">EXAMPLES</span></span>

### <span data-ttu-id="b055a-112">Örnek 1: veritabanını dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="b055a-112">Example 1: Export a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credential $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $exportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="b055a-113">Bu örnek, $BlobName değişkeninde depolanan BLOB depolama alanına $DatabaseName değişkeninde depolanan adı içeren Azure SQL veritabanından dışarı aktarma işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="b055a-113">This example initiates an export process from the Azure SQL Database that has the name stored in the $DatabaseName variable to the Blob storage stored in the $BlobName variable.</span></span>

## <span data-ttu-id="b055a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b055a-114">PARAMETERS</span></span>

### <span data-ttu-id="b055a-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="b055a-115">-BlobName</span></span>
<span data-ttu-id="b055a-116">Bu cmdlet 'in veritabanını dışarı aktardığı Azure Blob deposunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b055a-116">Specifies the name of the Azure Blob storage into which this cmdlet exports the database.</span></span>

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

### <span data-ttu-id="b055a-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b055a-117">-DatabaseName</span></span>
<span data-ttu-id="b055a-118">Bu cmdlet 'in veri dışarı aktardığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b055a-118">Specifies the name of the database from which this cmdlet exports data.</span></span>

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

### <span data-ttu-id="b055a-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="b055a-119">-Profile</span></span>
<span data-ttu-id="b055a-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b055a-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b055a-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b055a-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b055a-122">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="b055a-122">-SqlConnectionContext</span></span>
<span data-ttu-id="b055a-123">Veritabanının bulunduğu sunucunun bağlantı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b055a-123">Specifies the connection context of a server that contains the database.</span></span>

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

### <span data-ttu-id="b055a-124">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="b055a-124">-StorageContainer</span></span>
<span data-ttu-id="b055a-125">Bu cmdlet 'in bir veritabanını dışarı aktardıkları blob öğesini içeren depolama kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b055a-125">Specifies the storage container that contains the Blob into which this cmdlet export a database.</span></span>

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

### <span data-ttu-id="b055a-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="b055a-126">-StorageContainerName</span></span>
<span data-ttu-id="b055a-127">Bu cmdlet 'in veritabanı dışarı aktardığı blob 'U içeren depolama kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b055a-127">Specifies the name of the storage container that contains the Blob into which this cmdlet exports a database.</span></span>

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

### <span data-ttu-id="b055a-128">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="b055a-128">-StorageContext</span></span>
<span data-ttu-id="b055a-129">BLOB depolama kapsayıcısı 'nın bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b055a-129">Specifies the context of the Blob storage container.</span></span>

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

### <span data-ttu-id="b055a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b055a-130">CommonParameters</span></span>
<span data-ttu-id="b055a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b055a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b055a-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b055a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b055a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b055a-133">INPUTS</span></span>

## <span data-ttu-id="b055a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b055a-134">OUTPUTS</span></span>

### <span data-ttu-id="b055a-135">Microsoft. Windowsazde. Commands. SqlDatabase. Services. ımportexportrequest</span><span class="sxs-lookup"><span data-stu-id="b055a-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="b055a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b055a-136">NOTES</span></span>

## <span data-ttu-id="b055a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b055a-137">RELATED LINKS</span></span>

[<span data-ttu-id="b055a-138">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="b055a-138">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="b055a-139">Veritabanını dışarı aktar</span><span class="sxs-lookup"><span data-stu-id="b055a-139">Export Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781282.aspx)

[<span data-ttu-id="b055a-140">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="b055a-140">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="b055a-141">Get-Azuressqldatabaseımportexportstatus</span><span class="sxs-lookup"><span data-stu-id="b055a-141">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="b055a-142">Start-Azuressqldatabaseimport</span><span class="sxs-lookup"><span data-stu-id="b055a-142">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


