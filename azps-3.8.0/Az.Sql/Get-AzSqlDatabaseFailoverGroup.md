---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097030"
---
# <span data-ttu-id="ac68e-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ac68e-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="ac68e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac68e-102">SYNOPSIS</span></span>
<span data-ttu-id="ac68e-103">Azure SQL veritabanı yük devretme gruplarını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="ac68e-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="ac68e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac68e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac68e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac68e-105">DESCRIPTION</span></span>
<span data-ttu-id="ac68e-106">Belirli bir Azure SQL veritabanı yük devretme grubunu alır veya sunucudaki yük devretme gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="ac68e-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="ac68e-107">Komutu yürütmek için yük devretme grubundaki sunucu kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ac68e-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="ac68e-108">Döndürülen değerler, belirtilen sunucunun yük devretme grubuna göre durumunu yansıtır.</span><span class="sxs-lookup"><span data-stu-id="ac68e-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="ac68e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac68e-109">EXAMPLES</span></span>

### <span data-ttu-id="ac68e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ac68e-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="ac68e-111">Sunucudaki tüm yük devretme gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="ac68e-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="ac68e-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ac68e-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="ac68e-113">Belirli bir yük devretme grubu edinin.</span><span class="sxs-lookup"><span data-stu-id="ac68e-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="ac68e-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ac68e-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="ac68e-115">"FG" ile başlayan bir sunucudaki tüm yük devretme gruplarını edinin.</span><span class="sxs-lookup"><span data-stu-id="ac68e-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="ac68e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac68e-116">PARAMETERS</span></span>

### <span data-ttu-id="ac68e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac68e-117">-DefaultProfile</span></span>
<span data-ttu-id="ac68e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ac68e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac68e-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="ac68e-119">-FailoverGroupName</span></span>
<span data-ttu-id="ac68e-120">Alınacak Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ac68e-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="ac68e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac68e-121">-ResourceGroupName</span></span>
<span data-ttu-id="ac68e-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ac68e-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ac68e-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ac68e-123">-ServerName</span></span>
<span data-ttu-id="ac68e-124">Yük devretme grubunun alınacağı Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="ac68e-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="ac68e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac68e-125">CommonParameters</span></span>
<span data-ttu-id="ac68e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac68e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac68e-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ac68e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac68e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac68e-128">INPUTS</span></span>

### <span data-ttu-id="ac68e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ac68e-129">System.String</span></span>

## <span data-ttu-id="ac68e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac68e-130">OUTPUTS</span></span>

### <span data-ttu-id="ac68e-131">Microsoft. Azure. Commands. Sql. FailoverGroup. model. Azuressqlfailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="ac68e-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="ac68e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac68e-132">NOTES</span></span>

## <span data-ttu-id="ac68e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac68e-133">RELATED LINKS</span></span>

[<span data-ttu-id="ac68e-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ac68e-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ac68e-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ac68e-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ac68e-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ac68e-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="ac68e-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ac68e-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="ac68e-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ac68e-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ac68e-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ac68e-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ac68e-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="ac68e-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)