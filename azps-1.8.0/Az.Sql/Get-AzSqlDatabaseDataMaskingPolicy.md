---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: b604f0c154b24f8d50e6b341b1f39f8592981793
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759039"
---
# <span data-ttu-id="97b39-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="97b39-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="97b39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97b39-102">SYNOPSIS</span></span>
<span data-ttu-id="97b39-103">Veritabanı için veri maskeleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="97b39-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="97b39-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97b39-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97b39-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97b39-105">DESCRIPTION</span></span>
<span data-ttu-id="97b39-106">**Get-AzSqlDatabaseDataMaskingPolicy** cmdlet 'i, BIR Azure SQL veritabanının veri maskeleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="97b39-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="97b39-107">Bu cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="97b39-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="97b39-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="97b39-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="97b39-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97b39-109">EXAMPLES</span></span>

### <span data-ttu-id="97b39-110">Örnek 1: Azure SQL veritabanı için veri maskeleme ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="97b39-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="97b39-111">Bu komut, sunucu server01 ResourceGroup01 kaynak grubundaki veri maskeleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="97b39-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="97b39-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97b39-112">PARAMETERS</span></span>

### <span data-ttu-id="97b39-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="97b39-113">-DatabaseName</span></span>
<span data-ttu-id="97b39-114">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b39-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="97b39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b39-115">-DefaultProfile</span></span>
<span data-ttu-id="97b39-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="97b39-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97b39-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b39-117">-ResourceGroupName</span></span>
<span data-ttu-id="97b39-118">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b39-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="97b39-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="97b39-119">-ServerName</span></span>
<span data-ttu-id="97b39-120">Veritabanının bulunduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b39-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="97b39-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="97b39-121">-Confirm</span></span>
<span data-ttu-id="97b39-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97b39-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97b39-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97b39-123">-WhatIf</span></span>
<span data-ttu-id="97b39-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97b39-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97b39-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97b39-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97b39-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b39-126">CommonParameters</span></span>
<span data-ttu-id="97b39-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97b39-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b39-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="97b39-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b39-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97b39-129">INPUTS</span></span>

### <span data-ttu-id="97b39-130">System. String</span><span class="sxs-lookup"><span data-stu-id="97b39-130">System.String</span></span>

## <span data-ttu-id="97b39-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97b39-131">OUTPUTS</span></span>

### <span data-ttu-id="97b39-132">Microsoft. Azure. Commands. Sql. Datamaskeleme. model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="97b39-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="97b39-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97b39-133">NOTES</span></span>

## <span data-ttu-id="97b39-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97b39-134">RELATED LINKS</span></span>

[<span data-ttu-id="97b39-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="97b39-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="97b39-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="97b39-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="97b39-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="97b39-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="97b39-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="97b39-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="97b39-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="97b39-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

