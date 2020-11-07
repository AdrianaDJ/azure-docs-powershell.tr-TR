---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 40a193e96bdfa3c209a15e4a7be801e6ce71a3a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765052"
---
# <span data-ttu-id="a4758-101">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4758-101">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="a4758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4758-102">SYNOPSIS</span></span>
<span data-ttu-id="a4758-103">Azure SQL veritabanı yük devretme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a4758-103">Removes an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4758-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4758-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4758-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4758-105">DESCRIPTION</span></span>
<span data-ttu-id="a4758-106">Bu komut, tüm veritabanlarını ve çoğaltma ilişkilerini olduğu gibi bırakarak, belirtilen adla yük devretme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a4758-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="a4758-107">DNS 'den dinleyici uç noktasının kaydı silinir.</span><span class="sxs-lookup"><span data-stu-id="a4758-107">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="a4758-108">Komutu yürütmek için yük devretme grubunun birincil sunucusu kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a4758-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="a4758-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4758-109">EXAMPLES</span></span>

### <span data-ttu-id="a4758-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a4758-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="a4758-111">Bir yük devretme grubunu kaldırma.</span><span class="sxs-lookup"><span data-stu-id="a4758-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="a4758-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4758-112">PARAMETERS</span></span>

### <span data-ttu-id="a4758-113">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="a4758-113">-FailoverGroupName</span></span>
<span data-ttu-id="a4758-114">Kaldırılacak Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a4758-114">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="a4758-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a4758-115">-Force</span></span>
<span data-ttu-id="a4758-116">Eylemi gerçekleştirmek için onay iletisini atlayın.</span><span class="sxs-lookup"><span data-stu-id="a4758-116">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="a4758-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4758-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4758-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a4758-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4758-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a4758-119">-ServerName</span></span>
<span data-ttu-id="a4758-120">Yük devretme grubundaki birincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="a4758-120">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="a4758-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="a4758-121">-Confirm</span></span>
<span data-ttu-id="a4758-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a4758-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4758-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4758-123">-WhatIf</span></span>
<span data-ttu-id="a4758-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a4758-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4758-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a4758-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4758-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4758-126">-DefaultProfile</span></span>
<span data-ttu-id="a4758-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a4758-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4758-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4758-128">CommonParameters</span></span>
<span data-ttu-id="a4758-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4758-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4758-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4758-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4758-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4758-131">INPUTS</span></span>

### <span data-ttu-id="a4758-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a4758-132">System.String</span></span>

## <span data-ttu-id="a4758-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4758-133">OUTPUTS</span></span>

### <span data-ttu-id="a4758-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="a4758-134">System.Object</span></span>

## <span data-ttu-id="a4758-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4758-135">NOTES</span></span>

## <span data-ttu-id="a4758-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4758-136">RELATED LINKS</span></span>

[<span data-ttu-id="a4758-137">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4758-137">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a4758-138">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4758-138">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a4758-139">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4758-139">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a4758-140">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4758-140">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="a4758-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4758-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="a4758-142">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4758-142">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a4758-143">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="a4758-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
