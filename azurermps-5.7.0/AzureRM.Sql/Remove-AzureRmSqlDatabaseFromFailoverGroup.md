---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: ba0203b328b1ae75b1f671ed3e9437a47657bb1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592874"
---
# <span data-ttu-id="c4ca9-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c4ca9-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="c4ca9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ca9-103">Bir Azure SQL veritabanı yük devretme grubundan bir veya birden çok veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4ca9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4ca9-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4ca9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4ca9-105">DESCRIPTION</span></span>
<span data-ttu-id="c4ca9-106">Belirtilen Azure SQL veritabanı yük devretme grubundan bir veya birden çok veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="c4ca9-107">Veritabanları ve çoğaltma ilişkileri bozulmadan bırakılır, ancak artık yük devretme grubu uç noktaları aracılığıyla erişilebilir olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>

<span data-ttu-id="c4ca9-108">'-Database ' parametresini dolduracak veritabanı nesnelerini almak için, Get-AzureRmSqlDatabase cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="c4ca9-109">Komutu yürütmek için yük devretme grubunun birincil sunucusu kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="c4ca9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4ca9-110">EXAMPLES</span></span>

### <span data-ttu-id="c4ca9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c4ca9-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="c4ca9-112">Bu komut, bir veritabanını boru tarafından yük devretme grubundan çıkarır.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="c4ca9-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c4ca9-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzureRmSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="c4ca9-114">Bu komut, bir yük devretme grubundaki tüm veritabanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="c4ca9-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c4ca9-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzureRMSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="c4ca9-116">Bu komut, bir yük devretme grubundan elastik havuzda tüm veritabanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="c4ca9-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4ca9-117">PARAMETERS</span></span>

### <span data-ttu-id="c4ca9-118">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="c4ca9-118">-Database</span></span>
<span data-ttu-id="c4ca9-119">Yük devretme grubundaki birincil sunucusundaki bir veya birden çok Azure SQL veritabanı, yük devretme grubundan kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ca9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ca9-120">-DefaultProfile</span></span>
<span data-ttu-id="c4ca9-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c4ca9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4ca9-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ca9-122">-FailoverGroupName</span></span>
<span data-ttu-id="c4ca9-123">Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-123">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ca9-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c4ca9-124">-Force</span></span>
<span data-ttu-id="c4ca9-125">Eylemi gerçekleştirmek için onay iletisini atlayın.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="c4ca9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ca9-126">-ResourceGroupName</span></span>
<span data-ttu-id="c4ca9-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="c4ca9-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c4ca9-128">-ServerName</span></span>
<span data-ttu-id="c4ca9-129">Yük devretme grubundaki birincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="c4ca9-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="c4ca9-130">-Confirm</span></span>
<span data-ttu-id="c4ca9-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4ca9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4ca9-132">-WhatIf</span></span>
<span data-ttu-id="c4ca9-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4ca9-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4ca9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ca9-135">CommonParameters</span></span>
<span data-ttu-id="c4ca9-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4ca9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ca9-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4ca9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ca9-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4ca9-138">INPUTS</span></span>

### <span data-ttu-id="c4ca9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c4ca9-139">System.String</span></span>
<span data-ttu-id="c4ca9-140">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Sql. Database. model. Azurestabdatabasemodel, Microsoft. Azure. Commands. SQL, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c4ca9-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c4ca9-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4ca9-141">OUTPUTS</span></span>

### <span data-ttu-id="c4ca9-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="c4ca9-142">System.Object</span></span>

## <span data-ttu-id="c4ca9-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4ca9-143">NOTES</span></span>

## <span data-ttu-id="c4ca9-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4ca9-144">RELATED LINKS</span></span>

[<span data-ttu-id="c4ca9-145">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c4ca9-145">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c4ca9-146">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c4ca9-146">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c4ca9-147">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c4ca9-147">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c4ca9-148">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c4ca9-148">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="c4ca9-149">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c4ca9-149">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c4ca9-150">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c4ca9-150">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c4ca9-151">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c4ca9-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
