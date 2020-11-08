---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106293"
---
# <span data-ttu-id="ec320-101">Get-AzureSqlDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="ec320-101">Get-AzureSqlDatabaseOperation</span></span>

## <span data-ttu-id="ec320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec320-102">SYNOPSIS</span></span>
<span data-ttu-id="ec320-103">Bir Azure sunucusundaki veritabanı işlemlerinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ec320-103">Gets the status of database operations on an Azure server.</span></span>

## <span data-ttu-id="ec320-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec320-104">SYNTAX</span></span>

### <span data-ttu-id="ec320-105">ByConnectionContext (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec320-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ec320-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="ec320-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ec320-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec320-107">DESCRIPTION</span></span>
<span data-ttu-id="ec320-108">**Get-Azuressqldatabaseoperation** cmdlet 'ı belirtilen Azure sunucusundaki veritabanı işlemlerinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ec320-108">The **Get-AzureSqlDatabaseOperation** cmdlet gets the status of database operations on the specified Azure server.</span></span>
<span data-ttu-id="ec320-109">Yalnızca *ServerName* veya *ConnectionContext* parametresini belirtirseniz cmdlet, sunucunun tüm veritabanı işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="ec320-109">If you specify only the *ServerName* or *ConnectionContext* parameter, the cmdlet gets all the database operations for the server.</span></span>
<span data-ttu-id="ec320-110">*Veritabanı* veya *DatabaseName* parametresini kullanarak bir veritabanı belirtirseniz, bu cmdlet belirtilen veritabanı için tüm işlemleri alır.</span><span class="sxs-lookup"><span data-stu-id="ec320-110">If you also specify a database by using the *Database* or *DatabaseName* parameter, this cmdlet gets all the operations for the specified database.</span></span>
<span data-ttu-id="ec320-111">Bir işlem GUID 'si ve *ServerName* veya *ConnectionContext* belirtirseniz cmdlet tek bir veritabanı işlemini alır.</span><span class="sxs-lookup"><span data-stu-id="ec320-111">If you specify an operation GUID, and *ServerName* or *ConnectionContext* , the cmdlet gets a single database operation.</span></span>

## <span data-ttu-id="ec320-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec320-112">EXAMPLES</span></span>

### <span data-ttu-id="ec320-113">Örnek 1: veritabanı için tüm veritabanı işlemlerinin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="ec320-113">Example 1: Get the status of all database operations for a database</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

<span data-ttu-id="ec320-114">Bu komut, Database17 adlı sunucudaki, bağlantı bağlamının $Context belirttiği tüm veritabanı işlemlerinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ec320-114">This command gets the status of all database operations on the database named Database17 on the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="ec320-115">Örnek 2: sunucunun tüm veritabanı işlemlerinin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="ec320-115">Example 2: Get the status of all database operations for a server</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

<span data-ttu-id="ec320-116">Bu komut, sunucudaki bağlantı $Context bağlamının belirttiği tüm veritabanı işlemlerinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ec320-116">This command gets the status of all database operations on the server that the connection context $Context specifies.</span></span>

## <span data-ttu-id="ec320-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec320-117">PARAMETERS</span></span>

### <span data-ttu-id="ec320-118">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="ec320-118">-ConnectionContext</span></span>
<span data-ttu-id="ec320-119">Sunucunun bağlantı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec320-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec320-120">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="ec320-120">-Database</span></span>
<span data-ttu-id="ec320-121">Azure SQL veritabanını temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec320-121">Specifies an object that represents an Azure SQL Database.</span></span>
<span data-ttu-id="ec320-122">Bu parametreyi belirtirseniz, *ServerName* parametresini veya *ConnectionContext* parametresini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec320-122">If you specify this parameter, you must specify the *ServerName* parameter or *ConnectionContext* parameter.</span></span>

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec320-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ec320-123">-DatabaseName</span></span>
<span data-ttu-id="ec320-124">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec320-124">Specifies the name of a database.</span></span>
<span data-ttu-id="ec320-125">Bu parametreyi belirtirseniz, *ServerName* parametresini veya *ConnectionContext* parametresini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec320-125">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec320-126">-OperationGuid</span><span class="sxs-lookup"><span data-stu-id="ec320-126">-OperationGuid</span></span>
<span data-ttu-id="ec320-127">Bu cmdlet 'in durumu aldığı belirli bir veritabanı işlemini temsil eden işlem KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec320-127">Specifies the operation ID that represents a specific database operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="ec320-128">Azure SQL veritabanı veya sunucusu için tüm veritabanı işlemlerini isteyerek işlem kimlikleri elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec320-128">You can obtain operation IDs by requesting all the database operations for a Azure SQL Database or server.</span></span>
<span data-ttu-id="ec320-129">Bu parametreyi belirtirseniz, *ServerName* parametresini veya *ConnectionContext* parametresini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec320-129">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec320-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="ec320-130">-Profile</span></span>
<span data-ttu-id="ec320-131">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec320-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec320-132">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ec320-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec320-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ec320-133">-ServerName</span></span>
<span data-ttu-id="ec320-134">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec320-134">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec320-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec320-135">CommonParameters</span></span>
<span data-ttu-id="ec320-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec320-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec320-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec320-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec320-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec320-138">INPUTS</span></span>

### <span data-ttu-id="ec320-139">Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="ec320-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="ec320-140">Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="ec320-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

### <span data-ttu-id="ec320-141">System. Guid</span><span class="sxs-lookup"><span data-stu-id="ec320-141">System.Guid</span></span>

## <span data-ttu-id="ec320-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec320-142">OUTPUTS</span></span>

### <span data-ttu-id="ec320-143">Microsoft. Windowsazve. Commands. SqlDatabase. Services. Server. veritabanı. DatabaseOperationResponseList []</span><span class="sxs-lookup"><span data-stu-id="ec320-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponseList[]</span></span>
<span data-ttu-id="ec320-144">Bu cmdlet birden fazla işlem alırsanız **Databaseoperationresponselist** nesnelerinin dizisini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec320-144">This cmdlet returns an array of **DatabaseOperationResponseList** objects if you get multiple operations.</span></span>

### <span data-ttu-id="ec320-145">Microsoft. Windowsazve. Commands. SqlDatabase. Services. Server. veritabanı. DatabaseOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ec320-145">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponse</span></span>

## <span data-ttu-id="ec320-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec320-146">NOTES</span></span>

## <span data-ttu-id="ec320-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec320-147">RELATED LINKS</span></span>

[<span data-ttu-id="ec320-148">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="ec320-148">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="ec320-149">Veritabanı Işlemi durumu</span><span class="sxs-lookup"><span data-stu-id="ec320-149">Database Operation Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[<span data-ttu-id="ec320-150">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="ec320-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="ec320-151">Get-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="ec320-151">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="ec320-152">New-Azuressqldatabaseservercontext</span><span class="sxs-lookup"><span data-stu-id="ec320-152">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


