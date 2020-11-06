---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 9ffccf1122ac9919758883100eacce7933f5fea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589055"
---
# <span data-ttu-id="cb739-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="cb739-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="cb739-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb739-102">SYNOPSIS</span></span>
<span data-ttu-id="cb739-103">Geri yüklediğiniz silinmiş bir veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="cb739-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb739-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb739-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb739-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb739-105">DESCRIPTION</span></span>
<span data-ttu-id="cb739-106">**Get-AzureRMSqlDeletedDatabaseBackup** cmdlet 'i geri yükleyebilir veya geri yüklediğiniz tüm silinmiş yedekleme işlemlerini geri yükleyebilir.</span><span class="sxs-lookup"><span data-stu-id="cb739-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>

<span data-ttu-id="cb739-107">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="cb739-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cb739-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb739-108">EXAMPLES</span></span>

### <span data-ttu-id="cb739-109">Örnek 1: sunucudaki tüm silinmiş veritabanı yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="cb739-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="cb739-110">Bu komut, sunucudaki tüm silinmiş veritabanı yedeklemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="cb739-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="cb739-111">Örnek 2: belirtilen silinmiş veritabanı yedeklemesini alma</span><span class="sxs-lookup"><span data-stu-id="cb739-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="cb739-112">Bu komut, ContosoDatabase için silinmiş veritabanı yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="cb739-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="cb739-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb739-113">PARAMETERS</span></span>

### <span data-ttu-id="cb739-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cb739-114">-DatabaseName</span></span>
<span data-ttu-id="cb739-115">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb739-115">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="cb739-116">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="cb739-116">-DeletionDate</span></span>
<span data-ttu-id="cb739-117">Tarih **saat** nesnesi olarak, veritabanının silindiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb739-117">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="cb739-118">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb739-118">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="cb739-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb739-119">-ResourceGroupName</span></span>
<span data-ttu-id="cb739-120">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb739-120">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="cb739-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb739-121">-ServerName</span></span>
<span data-ttu-id="cb739-122">Veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb739-122">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="cb739-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="cb739-123">-Confirm</span></span>
<span data-ttu-id="cb739-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cb739-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb739-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb739-125">-WhatIf</span></span>
<span data-ttu-id="cb739-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb739-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb739-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cb739-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb739-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb739-128">-DefaultProfile</span></span>
<span data-ttu-id="cb739-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb739-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb739-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb739-130">CommonParameters</span></span>
<span data-ttu-id="cb739-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb739-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb739-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb739-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb739-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb739-133">INPUTS</span></span>

## <span data-ttu-id="cb739-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb739-134">OUTPUTS</span></span>

## <span data-ttu-id="cb739-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb739-135">NOTES</span></span>

## <span data-ttu-id="cb739-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb739-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb739-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb739-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="cb739-138">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="cb739-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
