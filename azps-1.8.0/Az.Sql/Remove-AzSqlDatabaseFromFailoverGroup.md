---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 4a39cd97936ef72615e30072de1988304fc5ad09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758859"
---
# <span data-ttu-id="bc9a3-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bc9a3-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="bc9a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="bc9a3-103">Bir Azure SQL veritabanı yük devretme grubundan bir veya birden çok veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="bc9a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc9a3-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc9a3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc9a3-105">DESCRIPTION</span></span>
<span data-ttu-id="bc9a3-106">Belirtilen Azure SQL veritabanı yük devretme grubundan bir veya birden çok veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="bc9a3-107">Veritabanları ve çoğaltma ilişkileri bozulmadan bırakılır, ancak artık yük devretme grubu uç noktaları aracılığıyla erişilebilir olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="bc9a3-108">'-Database ' parametresini dolduracak veritabanı nesnelerini almak için, Get-AzSqlDatabase cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="bc9a3-109">Komutu yürütmek için yük devretme grubunun birincil sunucusu kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="bc9a3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc9a3-110">EXAMPLES</span></span>

### <span data-ttu-id="bc9a3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bc9a3-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="bc9a3-112">Bu komut, bir veritabanını boru tarafından yük devretme grubundan çıkarır.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="bc9a3-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bc9a3-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="bc9a3-114">Bu komut, bir yük devretme grubundaki tüm veritabanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="bc9a3-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="bc9a3-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="bc9a3-116">Bu komut, bir yük devretme grubundan elastik havuzda tüm veritabanlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="bc9a3-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc9a3-117">PARAMETERS</span></span>

### <span data-ttu-id="bc9a3-118">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="bc9a3-118">-Database</span></span>
<span data-ttu-id="bc9a3-119">Yük devretme grubundaki birincil sunucusundaki bir veya birden çok Azure SQL veritabanı, yük devretme grubundan kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="bc9a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc9a3-120">-DefaultProfile</span></span>
<span data-ttu-id="bc9a3-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bc9a3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc9a3-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="bc9a3-122">-FailoverGroupName</span></span>
<span data-ttu-id="bc9a3-123">Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-123">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc9a3-124">-Force</span><span class="sxs-lookup"><span data-stu-id="bc9a3-124">-Force</span></span>
<span data-ttu-id="bc9a3-125">Eylemi gerçekleştirmek için onay iletisini atlayın.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-125">Skip confirmation message for performing the action.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc9a3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc9a3-126">-ResourceGroupName</span></span>
<span data-ttu-id="bc9a3-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="bc9a3-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bc9a3-128">-ServerName</span></span>
<span data-ttu-id="bc9a3-129">Yük devretme grubundaki birincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="bc9a3-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc9a3-130">-Confirm</span></span>
<span data-ttu-id="bc9a3-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc9a3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc9a3-132">-WhatIf</span></span>
<span data-ttu-id="bc9a3-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc9a3-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc9a3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc9a3-135">CommonParameters</span></span>
<span data-ttu-id="bc9a3-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc9a3-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bc9a3-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc9a3-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc9a3-138">INPUTS</span></span>

### <span data-ttu-id="bc9a3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bc9a3-139">System.String</span></span>

### <span data-ttu-id="bc9a3-140">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Sql. Database. model. Azurestabdatabasemodel, Microsoft. Azure. PowerShell. cmdlet. SQL, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bc9a3-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bc9a3-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc9a3-141">OUTPUTS</span></span>

### <span data-ttu-id="bc9a3-142">Microsoft. Azure. Commands. Sql. FailoverGroup. model. Azuressqlfailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="bc9a3-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="bc9a3-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc9a3-143">NOTES</span></span>

## <span data-ttu-id="bc9a3-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc9a3-144">RELATED LINKS</span></span>

[<span data-ttu-id="bc9a3-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bc9a3-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bc9a3-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bc9a3-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bc9a3-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bc9a3-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bc9a3-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bc9a3-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="bc9a3-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bc9a3-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bc9a3-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bc9a3-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bc9a3-151">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="bc9a3-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)