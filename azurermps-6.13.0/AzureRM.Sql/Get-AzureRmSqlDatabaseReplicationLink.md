---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
ms.openlocfilehash: 993d7ef8958e96cebcd104d25550e860cdfd1853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592728"
---
# <span data-ttu-id="93630-101">Get-AzureRmSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="93630-101">Get-AzureRmSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="93630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93630-102">SYNOPSIS</span></span>
<span data-ttu-id="93630-103">Azure SQL veritabanı ile kaynak grubu veya SQL Server arasındaki coğrafi çoğaltma bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="93630-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93630-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93630-104">SYNTAX</span></span>

### <span data-ttu-id="93630-105">ByRef (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="93630-105">ByDatabaseName (Default)</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93630-106">ByPartnerServerName</span><span class="sxs-lookup"><span data-stu-id="93630-106">ByPartnerServerName</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93630-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="93630-107">DESCRIPTION</span></span>
<span data-ttu-id="93630-108">**Get-AzureRMSqlDatabaseReplicationLink** cmdlet 'i **Get-Azuressqldatabasecopy** cmdlet 'ini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="93630-108">The **Get-AzureRMSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="93630-109">Belirtilen Azure SQL veritabanı ile kaynak grubu veya AzureSQL sunucusu arasındaki tüm coğrafi çoğaltma bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="93630-109">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="93630-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93630-110">EXAMPLES</span></span>

## <span data-ttu-id="93630-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93630-111">PARAMETERS</span></span>

### <span data-ttu-id="93630-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="93630-112">-DatabaseName</span></span>
<span data-ttu-id="93630-113">Bağlantıların alınacağı SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93630-113">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="93630-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93630-114">-DefaultProfile</span></span>
<span data-ttu-id="93630-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="93630-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93630-116">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93630-116">-PartnerResourceGroupName</span></span>
<span data-ttu-id="93630-117">Ortağın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93630-117">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="93630-118">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="93630-118">-PartnerServerName</span></span>
<span data-ttu-id="93630-119">İş ortağı için Azure SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93630-119">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPartnerServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93630-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93630-120">-ResourceGroupName</span></span>
<span data-ttu-id="93630-121">Bağlantıların alınacağı veritabanı için Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93630-121">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="93630-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="93630-122">-ServerName</span></span>
<span data-ttu-id="93630-123">Veritabanının bağlantılarının alınacağı SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93630-123">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="93630-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="93630-124">-Confirm</span></span>
<span data-ttu-id="93630-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="93630-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93630-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93630-126">-WhatIf</span></span>
<span data-ttu-id="93630-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="93630-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93630-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="93630-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93630-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93630-129">CommonParameters</span></span>
<span data-ttu-id="93630-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93630-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93630-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93630-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93630-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93630-132">INPUTS</span></span>

### <span data-ttu-id="93630-133">System. String</span><span class="sxs-lookup"><span data-stu-id="93630-133">System.String</span></span>

## <span data-ttu-id="93630-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93630-134">OUTPUTS</span></span>

### <span data-ttu-id="93630-135">Microsoft. Azure. Commands. Sql. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="93630-135">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="93630-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93630-136">NOTES</span></span>

## <span data-ttu-id="93630-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93630-137">RELATED LINKS</span></span>

[<span data-ttu-id="93630-138">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="93630-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
