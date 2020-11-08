---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106108"
---
# <span data-ttu-id="b8164-101">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8164-101">Remove-AzureSqlDatabase</span></span>

## <span data-ttu-id="b8164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8164-102">SYNOPSIS</span></span>
<span data-ttu-id="b8164-103">Azure SQL veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="b8164-103">Deletes an Azure SQL Database.</span></span>

## <span data-ttu-id="b8164-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8164-104">SYNTAX</span></span>

### <span data-ttu-id="b8164-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="b8164-105">ByNameWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8164-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="b8164-106">ByObjectWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8164-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="b8164-107">ByNameWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8164-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="b8164-108">ByObjectWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8164-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8164-109">DESCRIPTION</span></span>
<span data-ttu-id="b8164-110">**Remove-Azurestabanı** cmdlet 'i, BIR Azure SQL veritabanını sunucu bağlantısı bağlamı veya sunucu adı ile siler.</span><span class="sxs-lookup"><span data-stu-id="b8164-110">The **Remove-AzureSqlDatabase** cmdlet deletes an Azure SQL Database by server connection context or server name.</span></span>
<span data-ttu-id="b8164-111">**New-Azuressqldatabaseservercontext** cmdlet 'Ini kullanarak Azure SQL veritabanı sunucusu bağlantı bağlamını oluşturabilir ve bu cmdlet ile kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b8164-111">You can create an Azure SQL Database server connection context using the **New-AzureSqlDatabaseServerContext** cmdlet, and then use it with this cmdlet.</span></span>

<span data-ttu-id="b8164-112">Bir Azure SQL veritabanı sunucusu adı belirterek bir veritabanını sildiğinizde, **Remove-Azuresurdatabase** cmdlet 'i, işlemi gerçekleştirmek için adı ve geçerli Azure aboneliği bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b8164-112">When you delete a database by specifying an Azure SQL Database server name, the **Remove-AzureSqlDatabase** cmdlet uses the name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="b8164-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8164-113">EXAMPLES</span></span>

### <span data-ttu-id="b8164-114">Örnek 1: veritabanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b8164-114">Example 1: Remove a database</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="b8164-115">Bu komut, Database01 adlı veritabanını Azure SQL veritabanı sunucusu bağlantı bağlamı $Context kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b8164-115">This command removes the database named Database01 from the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="b8164-116">Örnek 2: sunucu adı kullanarak veritabanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b8164-116">Example 2: Remove a database by using a server name</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="b8164-117">Bu komut, Database01 adlı Azure SQL veritabanı sunucusundan gelen veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b8164-117">This command removes the database named Database01 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="b8164-118">Örnek 3: ardışık düzeni kullanarak veritabanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b8164-118">Example 3: Remove a database by using the pipeline</span></span>
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="b8164-119">Bu örnek, ardışık düzen aracılığıyla veritabanı nesnesini geçirmenin alternatif yöntemini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8164-119">This example demonstrates the alternative method of passing the database object through the pipeline.</span></span>

## <span data-ttu-id="b8164-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8164-120">PARAMETERS</span></span>

### <span data-ttu-id="b8164-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="b8164-121">-ConnectionContext</span></span>
<span data-ttu-id="b8164-122">Bu cmdlet 'in veritabanından kaldırıldığı sunucunun bağlantı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8164-122">Specifies the connection context of a server from which this cmdlet removes a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8164-123">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="b8164-123">-Database</span></span>
<span data-ttu-id="b8164-124">Bu cmdlet 'in kaldırdığı veritabanını temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8164-124">Specifies an object that represents the database that this cmdlet removes.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8164-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8164-125">-DatabaseName</span></span>
<span data-ttu-id="b8164-126">Bu cmdlet 'in kaldırdığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8164-126">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8164-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b8164-127">-Force</span></span>
<span data-ttu-id="b8164-128">Eylemin kullanıcıya onay istemeden yapılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="b8164-128">Allows the action to complete without prompting the user for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8164-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="b8164-129">-Profile</span></span>
<span data-ttu-id="b8164-130">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8164-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b8164-131">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b8164-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b8164-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b8164-132">-ServerName</span></span>
<span data-ttu-id="b8164-133">Bu cmdlet 'in veritabanını sildiği sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8164-133">Specifies the name of the server on which this cmdlet deletes the database.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8164-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="b8164-134">-Confirm</span></span>
<span data-ttu-id="b8164-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b8164-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8164-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8164-136">-WhatIf</span></span>
<span data-ttu-id="b8164-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8164-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8164-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b8164-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8164-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8164-139">CommonParameters</span></span>
<span data-ttu-id="b8164-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8164-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8164-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8164-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8164-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8164-142">INPUTS</span></span>

### <span data-ttu-id="b8164-143">Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="b8164-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="b8164-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8164-144">OUTPUTS</span></span>

## <span data-ttu-id="b8164-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8164-145">NOTES</span></span>
* <span data-ttu-id="b8164-146">İşlemin önem derecesi nedeniyle, bu cmdlet varsayılan olarak sizden onay ister.</span><span class="sxs-lookup"><span data-stu-id="b8164-146">Because of the severity of the operation, by default, this cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="b8164-147">Onayı atlamak için *Force* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b8164-147">To skip confirmation, specify the *Force* parameter.</span></span>

## <span data-ttu-id="b8164-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8164-148">RELATED LINKS</span></span>

[<span data-ttu-id="b8164-149">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="b8164-149">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="b8164-150">Veritabanını sil</span><span class="sxs-lookup"><span data-stu-id="b8164-150">Delete Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[<span data-ttu-id="b8164-151">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="b8164-151">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="b8164-152">Get-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="b8164-152">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="b8164-153">Yeni-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="b8164-153">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="b8164-154">New-Azuressqldatabaseservercontext</span><span class="sxs-lookup"><span data-stu-id="b8164-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="b8164-155">Set-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="b8164-155">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


