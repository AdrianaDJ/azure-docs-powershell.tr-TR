---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106294"
---
# <span data-ttu-id="23d52-101">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="23d52-101">Get-AzureSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="23d52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23d52-102">SYNOPSIS</span></span>
<span data-ttu-id="23d52-103">İçeri veya dışarı aktarma isteğinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="23d52-103">Gets the status of an import or export request.</span></span>

## <span data-ttu-id="23d52-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23d52-104">SYNTAX</span></span>

### <span data-ttu-id="23d52-105">Byconnectionınfo</span><span class="sxs-lookup"><span data-stu-id="23d52-105">ByConnectionInfo</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="23d52-106">ByRequestObject</span><span class="sxs-lookup"><span data-stu-id="23d52-106">ByRequestObject</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="23d52-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="23d52-107">DESCRIPTION</span></span>
<span data-ttu-id="23d52-108">**Get-Azureskurdatabaseımportexportstatus** cmdlet 'i içeri aktarma veya dışarı aktarma isteğinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="23d52-108">The **Get-AzureSqlDatabaseImportExportStatus** cmdlet gets the status of an import or export request.</span></span>
<span data-ttu-id="23d52-109">Start-AzureSqlDatabaseImport veya Start-AzureSqlDatabaseExport cmdlet 'i istekleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="23d52-109">The Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet initiates requests.</span></span>
<span data-ttu-id="23d52-110">Request nesnesini *Request* parametresini kullanarak belirtebilirsiniz veya *İstekKimliği RequestId* parametresini ve *Kullanıcı adı* , *parola* ve *ServerName* parametrelerini kullanarak tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23d52-110">You can specify the request object by using the *Request* parameter, or you can identify the request by using the *RequestId* parameter and the *Username* , *Password* , and *ServerName* parameters.</span></span>

## <span data-ttu-id="23d52-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23d52-111">EXAMPLES</span></span>

### <span data-ttu-id="23d52-112">Örnek 1: dışarı aktarma isteğinin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="23d52-112">Example 1: Get the status of an export request</span></span>
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

<span data-ttu-id="23d52-113">İlk komut bir dışarı aktarma isteği oluşturur ve $ExportRequest değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="23d52-113">The first command creates an export request, and then stores it in the $ExportRequest variable.</span></span>

<span data-ttu-id="23d52-114">İkinci komut $ExportRequest uygulamasında depolanan dışarı aktarma isteğinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="23d52-114">The second command gets the status of the export request stored in $ExportRequest.</span></span>

## <span data-ttu-id="23d52-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23d52-115">PARAMETERS</span></span>

### <span data-ttu-id="23d52-116">-Parola</span><span class="sxs-lookup"><span data-stu-id="23d52-116">-Password</span></span>
<span data-ttu-id="23d52-117">Azure SQL veritabanı sunucusuna bağlanmak için gereken parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="23d52-117">Specifies the password that is required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="23d52-118">*RequestId* parametresini belirttiyseniz bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="23d52-118">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d52-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="23d52-119">-Profile</span></span>
<span data-ttu-id="23d52-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23d52-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23d52-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="23d52-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23d52-122">-İstek</span><span class="sxs-lookup"><span data-stu-id="23d52-122">-Request</span></span>
<span data-ttu-id="23d52-123">**Importexportrequest** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23d52-123">Specifies an **ImportExportRequest** object.</span></span>
<span data-ttu-id="23d52-124">İçeri veya dışarı aktarma isteği nesnesi almak için Start-AzureSqlDatabaseImport veya Start-AzureSqlDatabaseExport cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="23d52-124">To obtain an import or export request object, use the Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet.</span></span>

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d52-125">-RequestId</span><span class="sxs-lookup"><span data-stu-id="23d52-125">-RequestId</span></span>
<span data-ttu-id="23d52-126">Bu cmdlet 'in durumu aldığı içeri veya dışarı aktarma işleminin GUID 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23d52-126">Specifies the GUID of the import or export operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="23d52-127">Bu parametreyi belirtirseniz *Kullanıcı adı* , *parola* ve *ServerName* parametrelerini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="23d52-127">If you specify this parameter, you must specify the *UserName* , *Password* , and *ServerName* parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d52-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="23d52-128">-ServerName</span></span>
<span data-ttu-id="23d52-129">Azure SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23d52-129">Specifies the name of the Azure SQL Database server.</span></span>
<span data-ttu-id="23d52-130">*RequestId* parametresini belirttiyseniz bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="23d52-130">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d52-131">-Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="23d52-131">-Username</span></span>
<span data-ttu-id="23d52-132">Azure SQL veritabanı sunucusuna bağlanmak için gereken kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23d52-132">Specifies the user name required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="23d52-133">*RequestId* parametresini belirttiyseniz bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="23d52-133">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d52-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d52-134">CommonParameters</span></span>
<span data-ttu-id="23d52-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23d52-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d52-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23d52-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d52-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23d52-137">INPUTS</span></span>

## <span data-ttu-id="23d52-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23d52-138">OUTPUTS</span></span>

### <span data-ttu-id="23d52-139">Microsoft. Windowsazde. Commands. SqlDatabase. Services. ımportexport. StatusInfo</span><span class="sxs-lookup"><span data-stu-id="23d52-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExport.StatusInfo</span></span>

## <span data-ttu-id="23d52-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23d52-140">NOTES</span></span>

## <span data-ttu-id="23d52-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23d52-141">RELATED LINKS</span></span>

[<span data-ttu-id="23d52-142">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="23d52-142">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="23d52-143">Içeri aktarma veritabanı durumunu alma</span><span class="sxs-lookup"><span data-stu-id="23d52-143">Get Import Export Database Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[<span data-ttu-id="23d52-144">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="23d52-144">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="23d52-145">Start-Azuressqldatabaseexport</span><span class="sxs-lookup"><span data-stu-id="23d52-145">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)

[<span data-ttu-id="23d52-146">Start-Azuressqldatabaseimport</span><span class="sxs-lookup"><span data-stu-id="23d52-146">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


