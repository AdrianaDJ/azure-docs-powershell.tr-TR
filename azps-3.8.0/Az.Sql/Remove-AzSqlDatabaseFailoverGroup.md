---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098686"
---
# <span data-ttu-id="1481e-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1481e-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="1481e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1481e-102">SYNOPSIS</span></span>
<span data-ttu-id="1481e-103">Azure SQL veritabanı yük devretme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1481e-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="1481e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1481e-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1481e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1481e-105">DESCRIPTION</span></span>
<span data-ttu-id="1481e-106">Bu komut, tüm veritabanlarını ve çoğaltma ilişkilerini olduğu gibi bırakarak, belirtilen adla yük devretme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1481e-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="1481e-107">DNS 'den dinleyici uç noktasının kaydı silinir.</span><span class="sxs-lookup"><span data-stu-id="1481e-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="1481e-108">Komutu yürütmek için yük devretme grubunun birincil sunucusu kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1481e-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="1481e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1481e-109">EXAMPLES</span></span>

### <span data-ttu-id="1481e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1481e-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="1481e-111">Bir yük devretme grubunu kaldırma.</span><span class="sxs-lookup"><span data-stu-id="1481e-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="1481e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1481e-112">PARAMETERS</span></span>

### <span data-ttu-id="1481e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1481e-113">-DefaultProfile</span></span>
<span data-ttu-id="1481e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1481e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1481e-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="1481e-115">-FailoverGroupName</span></span>
<span data-ttu-id="1481e-116">Kaldırılacak Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1481e-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="1481e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1481e-117">-Force</span></span>
<span data-ttu-id="1481e-118">Eylemi gerçekleştirmek için onay iletisini atlayın.</span><span class="sxs-lookup"><span data-stu-id="1481e-118">Skip confirmation message for performing the action.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1481e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1481e-119">-ResourceGroupName</span></span>
<span data-ttu-id="1481e-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1481e-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="1481e-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1481e-121">-ServerName</span></span>
<span data-ttu-id="1481e-122">Yük devretme grubundaki birincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="1481e-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="1481e-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="1481e-123">-Confirm</span></span>
<span data-ttu-id="1481e-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1481e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1481e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1481e-125">-WhatIf</span></span>
<span data-ttu-id="1481e-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1481e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1481e-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1481e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1481e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1481e-128">CommonParameters</span></span>
<span data-ttu-id="1481e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1481e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1481e-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1481e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1481e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1481e-131">INPUTS</span></span>

### <span data-ttu-id="1481e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1481e-132">System.String</span></span>

## <span data-ttu-id="1481e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1481e-133">OUTPUTS</span></span>

### <span data-ttu-id="1481e-134">Microsoft. Azure. Commands. Sql. FailoverGroup. model. Azuressqlfailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="1481e-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="1481e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1481e-135">NOTES</span></span>

## <span data-ttu-id="1481e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1481e-136">RELATED LINKS</span></span>

[<span data-ttu-id="1481e-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1481e-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1481e-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1481e-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1481e-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1481e-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1481e-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1481e-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="1481e-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1481e-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="1481e-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1481e-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1481e-143">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="1481e-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
