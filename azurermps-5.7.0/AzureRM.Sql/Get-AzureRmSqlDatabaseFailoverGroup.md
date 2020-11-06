---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a4440601610af0b55282cbe0e78209379f570edb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573205"
---
# <span data-ttu-id="98c4f-101">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c4f-101">Get-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="98c4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="98c4f-103">Azure SQL veritabanı yük devretme gruplarını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="98c4f-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98c4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98c4f-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98c4f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="98c4f-106">Belirli bir Azure SQL veritabanı yük devretme grubunu alır veya sunucudaki yük devretme gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="98c4f-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>

<span data-ttu-id="98c4f-107">Komutu yürütmek için yük devretme grubundaki sunucu kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="98c4f-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="98c4f-108">Döndürülen değerler, belirtilen sunucunun yük devretme grubuna göre durumunu yansıtır.</span><span class="sxs-lookup"><span data-stu-id="98c4f-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="98c4f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98c4f-109">EXAMPLES</span></span>

### <span data-ttu-id="98c4f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="98c4f-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="98c4f-111">Sunucudaki tüm yük devretme gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="98c4f-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="98c4f-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="98c4f-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="98c4f-113">Belirli bir yük devretme grubu edinin.</span><span class="sxs-lookup"><span data-stu-id="98c4f-113">Get a specific Failover Group.</span></span>

## <span data-ttu-id="98c4f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98c4f-114">PARAMETERS</span></span>

### <span data-ttu-id="98c4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c4f-115">-DefaultProfile</span></span>
<span data-ttu-id="98c4f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="98c4f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98c4f-117">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="98c4f-117">-FailoverGroupName</span></span>
<span data-ttu-id="98c4f-118">Alınacak Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="98c4f-118">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="98c4f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c4f-119">-ResourceGroupName</span></span>
<span data-ttu-id="98c4f-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="98c4f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="98c4f-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="98c4f-121">-ServerName</span></span>
<span data-ttu-id="98c4f-122">Yük devretme grubunun alınacağı Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="98c4f-122">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="98c4f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c4f-123">CommonParameters</span></span>
<span data-ttu-id="98c4f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98c4f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c4f-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c4f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c4f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98c4f-126">INPUTS</span></span>

### <span data-ttu-id="98c4f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="98c4f-127">System.String</span></span>

## <span data-ttu-id="98c4f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98c4f-128">OUTPUTS</span></span>

### <span data-ttu-id="98c4f-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="98c4f-129">System.Object</span></span>

## <span data-ttu-id="98c4f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98c4f-130">NOTES</span></span>

## <span data-ttu-id="98c4f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98c4f-131">RELATED LINKS</span></span>

[<span data-ttu-id="98c4f-132">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c4f-132">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="98c4f-133">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c4f-133">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="98c4f-134">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c4f-134">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="98c4f-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c4f-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="98c4f-136">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c4f-136">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="98c4f-137">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98c4f-137">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="98c4f-138">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="98c4f-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
