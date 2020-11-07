---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
ms.openlocfilehash: 6bb2a3891abe8453ee8460f6879dbc134f6ab29b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933662"
---
# <span data-ttu-id="aeb80-101">Get-AzSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="aeb80-101">Get-AzSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="aeb80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeb80-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb80-103">Azure SQL veritabanı ile kaynak grubu veya SQL Server arasındaki coğrafi çoğaltma bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="aeb80-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

## <span data-ttu-id="aeb80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aeb80-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeb80-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aeb80-105">DESCRIPTION</span></span>
<span data-ttu-id="aeb80-106">**Get-AzSqlDatabaseReplicationLink** cmdlet 'i **Get-AzSqlDatabaseCopy** cmdlet 'ini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="aeb80-106">The **Get-AzSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="aeb80-107">Belirtilen Azure SQL veritabanı ile kaynak grubu veya AzureSQL sunucusu arasındaki tüm coğrafi çoğaltma bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="aeb80-107">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="aeb80-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aeb80-108">EXAMPLES</span></span>

## <span data-ttu-id="aeb80-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aeb80-109">PARAMETERS</span></span>

### <span data-ttu-id="aeb80-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aeb80-110">-DatabaseName</span></span>
<span data-ttu-id="aeb80-111">Bağlantıların alınacağı SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb80-111">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="aeb80-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeb80-112">-DefaultProfile</span></span>
<span data-ttu-id="aeb80-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="aeb80-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aeb80-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeb80-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="aeb80-115">Ortağın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb80-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb80-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="aeb80-116">-PartnerServerName</span></span>
<span data-ttu-id="aeb80-117">İş ortağı için Azure SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb80-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="aeb80-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeb80-118">-ResourceGroupName</span></span>
<span data-ttu-id="aeb80-119">Bağlantıların alınacağı veritabanı için Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb80-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="aeb80-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aeb80-120">-ServerName</span></span>
<span data-ttu-id="aeb80-121">Veritabanının bağlantılarının alınacağı SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeb80-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="aeb80-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="aeb80-122">-Confirm</span></span>
<span data-ttu-id="aeb80-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aeb80-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb80-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeb80-124">-WhatIf</span></span>
<span data-ttu-id="aeb80-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aeb80-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aeb80-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aeb80-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb80-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb80-127">CommonParameters</span></span>
<span data-ttu-id="aeb80-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aeb80-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb80-129">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aeb80-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb80-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aeb80-130">INPUTS</span></span>

### <span data-ttu-id="aeb80-131">System. String</span><span class="sxs-lookup"><span data-stu-id="aeb80-131">System.String</span></span>

## <span data-ttu-id="aeb80-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aeb80-132">OUTPUTS</span></span>

### <span data-ttu-id="aeb80-133">Microsoft. Azure. Commands. Sql. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="aeb80-133">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="aeb80-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aeb80-134">NOTES</span></span>

## <span data-ttu-id="aeb80-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aeb80-135">RELATED LINKS</span></span>

[<span data-ttu-id="aeb80-136">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="aeb80-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
