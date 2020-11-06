---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a6fd65ed16797d3d497160f7f7d9d52f17bd2f1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592879"
---
# <span data-ttu-id="a4059-101">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4059-101">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="a4059-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4059-102">SYNOPSIS</span></span>
<span data-ttu-id="a4059-103">Azure SQL veritabanı yük devretme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a4059-103">Removes an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4059-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4059-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4059-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4059-105">DESCRIPTION</span></span>
<span data-ttu-id="a4059-106">Bu komut, tüm veritabanlarını ve çoğaltma ilişkilerini olduğu gibi bırakarak, belirtilen adla yük devretme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a4059-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="a4059-107">DNS 'den dinleyici uç noktasının kaydı silinir.</span><span class="sxs-lookup"><span data-stu-id="a4059-107">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="a4059-108">Komutu yürütmek için yük devretme grubunun birincil sunucusu kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a4059-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="a4059-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4059-109">EXAMPLES</span></span>

### <span data-ttu-id="a4059-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a4059-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="a4059-111">Bir yük devretme grubunu kaldırma.</span><span class="sxs-lookup"><span data-stu-id="a4059-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="a4059-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4059-112">PARAMETERS</span></span>

### <span data-ttu-id="a4059-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4059-113">-DefaultProfile</span></span>
<span data-ttu-id="a4059-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a4059-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4059-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="a4059-115">-FailoverGroupName</span></span>
<span data-ttu-id="a4059-116">Kaldırılacak Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a4059-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="a4059-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a4059-117">-Force</span></span>
<span data-ttu-id="a4059-118">Eylemi gerçekleştirmek için onay iletisini atlayın.</span><span class="sxs-lookup"><span data-stu-id="a4059-118">Skip confirmation message for performing the action.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4059-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4059-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4059-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a4059-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4059-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a4059-121">-ServerName</span></span>
<span data-ttu-id="a4059-122">Yük devretme grubundaki birincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="a4059-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="a4059-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="a4059-123">-Confirm</span></span>
<span data-ttu-id="a4059-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a4059-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4059-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4059-125">-WhatIf</span></span>
<span data-ttu-id="a4059-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a4059-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4059-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a4059-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4059-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4059-128">CommonParameters</span></span>
<span data-ttu-id="a4059-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4059-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4059-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4059-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4059-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4059-131">INPUTS</span></span>

### <span data-ttu-id="a4059-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a4059-132">System.String</span></span>

## <span data-ttu-id="a4059-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4059-133">OUTPUTS</span></span>

### <span data-ttu-id="a4059-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="a4059-134">System.Object</span></span>

## <span data-ttu-id="a4059-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4059-135">NOTES</span></span>

## <span data-ttu-id="a4059-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4059-136">RELATED LINKS</span></span>

[<span data-ttu-id="a4059-137">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4059-137">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a4059-138">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4059-138">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a4059-139">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4059-139">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a4059-140">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4059-140">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="a4059-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4059-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="a4059-142">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4059-142">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a4059-143">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="a4059-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
