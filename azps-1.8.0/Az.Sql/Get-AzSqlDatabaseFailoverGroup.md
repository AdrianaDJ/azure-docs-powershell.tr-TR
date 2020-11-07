---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 430c4cc1318d53ebb2671b9fb1dd0cea8655898d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759036"
---
# <span data-ttu-id="6ae82-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6ae82-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="6ae82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ae82-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae82-103">Azure SQL veritabanı yük devretme gruplarını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="6ae82-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="6ae82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ae82-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ae82-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ae82-105">DESCRIPTION</span></span>
<span data-ttu-id="6ae82-106">Belirli bir Azure SQL veritabanı yük devretme grubunu alır veya sunucudaki yük devretme gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="6ae82-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="6ae82-107">Komutu yürütmek için yük devretme grubundaki sunucu kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6ae82-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="6ae82-108">Döndürülen değerler, belirtilen sunucunun yük devretme grubuna göre durumunu yansıtır.</span><span class="sxs-lookup"><span data-stu-id="6ae82-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="6ae82-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ae82-109">EXAMPLES</span></span>

### <span data-ttu-id="6ae82-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6ae82-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="6ae82-111">Sunucudaki tüm yük devretme gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="6ae82-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="6ae82-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6ae82-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="6ae82-113">Belirli bir yük devretme grubu edinin.</span><span class="sxs-lookup"><span data-stu-id="6ae82-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="6ae82-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="6ae82-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="6ae82-115">"FG" ile başlayan bir sunucudaki tüm yük devretme gruplarını edinin.</span><span class="sxs-lookup"><span data-stu-id="6ae82-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="6ae82-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ae82-116">PARAMETERS</span></span>

### <span data-ttu-id="6ae82-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ae82-117">-DefaultProfile</span></span>
<span data-ttu-id="6ae82-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6ae82-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ae82-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="6ae82-119">-FailoverGroupName</span></span>
<span data-ttu-id="6ae82-120">Alınacak Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6ae82-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6ae82-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ae82-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ae82-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6ae82-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="6ae82-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6ae82-123">-ServerName</span></span>
<span data-ttu-id="6ae82-124">Yük devretme grubunun alınacağı Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="6ae82-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="6ae82-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae82-125">CommonParameters</span></span>
<span data-ttu-id="6ae82-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ae82-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae82-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6ae82-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae82-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ae82-128">INPUTS</span></span>

### <span data-ttu-id="6ae82-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6ae82-129">System.String</span></span>

## <span data-ttu-id="6ae82-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ae82-130">OUTPUTS</span></span>

### <span data-ttu-id="6ae82-131">Microsoft. Azure. Commands. Sql. FailoverGroup. model. Azuressqlfailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="6ae82-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="6ae82-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ae82-132">NOTES</span></span>

## <span data-ttu-id="6ae82-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ae82-133">RELATED LINKS</span></span>

[<span data-ttu-id="6ae82-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6ae82-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6ae82-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6ae82-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6ae82-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6ae82-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="6ae82-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6ae82-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="6ae82-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6ae82-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6ae82-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6ae82-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6ae82-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="6ae82-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
