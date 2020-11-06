---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 2358383cd7cfdbf547ae14476e788d6919baacd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573229"
---
# <span data-ttu-id="c369d-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="c369d-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="c369d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c369d-102">SYNOPSIS</span></span>
<span data-ttu-id="c369d-103">Geri yüklediğiniz silinmiş bir veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="c369d-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c369d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c369d-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c369d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c369d-105">DESCRIPTION</span></span>
<span data-ttu-id="c369d-106">**Get-AzureRMSqlDeletedDatabaseBackup** cmdlet 'i geri yükleyebilir veya geri yüklediğiniz tüm silinmiş yedekleme işlemlerini geri yükleyebilir.</span><span class="sxs-lookup"><span data-stu-id="c369d-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>

<span data-ttu-id="c369d-107">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="c369d-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c369d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c369d-108">EXAMPLES</span></span>

### <span data-ttu-id="c369d-109">Örnek 1: sunucudaki tüm silinmiş veritabanı yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="c369d-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="c369d-110">Bu komut, sunucudaki tüm silinmiş veritabanı yedeklemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c369d-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="c369d-111">Örnek 2: belirtilen silinmiş veritabanı yedeklemesini alma</span><span class="sxs-lookup"><span data-stu-id="c369d-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="c369d-112">Bu komut, ContosoDatabase için silinmiş veritabanı yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="c369d-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="c369d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c369d-113">PARAMETERS</span></span>

### <span data-ttu-id="c369d-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c369d-114">-DatabaseName</span></span>
<span data-ttu-id="c369d-115">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c369d-115">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c369d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c369d-116">-DefaultProfile</span></span>
<span data-ttu-id="c369d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c369d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c369d-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="c369d-118">-DeletionDate</span></span>
<span data-ttu-id="c369d-119">Tarih **saat** nesnesi olarak, veritabanının silindiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c369d-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="c369d-120">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c369d-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c369d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c369d-121">-ResourceGroupName</span></span>
<span data-ttu-id="c369d-122">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c369d-122">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c369d-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c369d-123">-ServerName</span></span>
<span data-ttu-id="c369d-124">Veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c369d-124">Specifies the name of the database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c369d-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="c369d-125">-Confirm</span></span>
<span data-ttu-id="c369d-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c369d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c369d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c369d-127">-WhatIf</span></span>
<span data-ttu-id="c369d-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c369d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c369d-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c369d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c369d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c369d-130">CommonParameters</span></span>
<span data-ttu-id="c369d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c369d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c369d-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c369d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c369d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c369d-133">INPUTS</span></span>

### <span data-ttu-id="c369d-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c369d-134">None</span></span>
<span data-ttu-id="c369d-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c369d-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c369d-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c369d-136">OUTPUTS</span></span>

## <span data-ttu-id="c369d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c369d-137">NOTES</span></span>

## <span data-ttu-id="c369d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c369d-138">RELATED LINKS</span></span>

[<span data-ttu-id="c369d-139">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c369d-139">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="c369d-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c369d-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
