---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: d534ddc9c076d0e7c2ea611d6fdb15ae22e84846
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096996"
---
# <span data-ttu-id="cd7ff-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="cd7ff-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="cd7ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7ff-103">Geri yüklediğiniz silinmiş bir veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="cd7ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd7ff-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd7ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd7ff-105">DESCRIPTION</span></span>
<span data-ttu-id="cd7ff-106">**Get-AzSqlDeletedDatabaseBackup** cmdlet 'i, geri yüklediğiniz veya geri yüklediğiniz tüm silinmiş yedekleme işlemlerini geri yükleyebilir.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="cd7ff-107">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cd7ff-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd7ff-108">EXAMPLES</span></span>

### <span data-ttu-id="cd7ff-109">Örnek 1: sunucudaki tüm silinmiş veritabanı yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="cd7ff-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="cd7ff-110">Bu komut, sunucudaki tüm silinmiş veritabanı yedeklemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="cd7ff-111">Örnek 2: belirtilen silinmiş veritabanı yedeklemesini alma</span><span class="sxs-lookup"><span data-stu-id="cd7ff-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="cd7ff-112">Bu komut, ContosoDatabase için silinmiş veritabanı yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="cd7ff-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd7ff-113">PARAMETERS</span></span>

### <span data-ttu-id="cd7ff-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cd7ff-114">-DatabaseName</span></span>
<span data-ttu-id="cd7ff-115">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd7ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7ff-116">-DefaultProfile</span></span>
<span data-ttu-id="cd7ff-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cd7ff-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd7ff-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="cd7ff-118">-DeletionDate</span></span>
<span data-ttu-id="cd7ff-119">Tarih **saat** nesnesi olarak, veritabanının silindiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="cd7ff-120">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd7ff-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd7ff-121">-ResourceGroupName</span></span>
<span data-ttu-id="cd7ff-122">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-122">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd7ff-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cd7ff-123">-ServerName</span></span>
<span data-ttu-id="cd7ff-124">Veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-124">Specifies the name of the database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd7ff-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd7ff-125">-Confirm</span></span>
<span data-ttu-id="cd7ff-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd7ff-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd7ff-127">-WhatIf</span></span>
<span data-ttu-id="cd7ff-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd7ff-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd7ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7ff-130">CommonParameters</span></span>
<span data-ttu-id="cd7ff-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7ff-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cd7ff-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7ff-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd7ff-133">INPUTS</span></span>

### <span data-ttu-id="cd7ff-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cd7ff-134">System.String</span></span>

### <span data-ttu-id="cd7ff-135">System. Nullable ' 1 [[System. DATETIME, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="cd7ff-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cd7ff-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd7ff-136">OUTPUTS</span></span>

### <span data-ttu-id="cd7ff-137">Microsoft. Azure. Commands. Sql. Backup. model. Azuressqldeleteddatabasebackupmodel</span><span class="sxs-lookup"><span data-stu-id="cd7ff-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="cd7ff-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd7ff-138">NOTES</span></span>

## <span data-ttu-id="cd7ff-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd7ff-139">RELATED LINKS</span></span>

[<span data-ttu-id="cd7ff-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cd7ff-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="cd7ff-141">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="cd7ff-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
