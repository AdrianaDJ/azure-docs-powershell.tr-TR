---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: 4f90d6d0c33874750bf2f32ae7f65bf32457f63c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276707"
---
# <span data-ttu-id="6841a-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6841a-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="6841a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6841a-102">SYNOPSIS</span></span>
<span data-ttu-id="6841a-103">Bir veya daha fazla veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="6841a-103">Gets one or more databases.</span></span>

## <span data-ttu-id="6841a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6841a-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6841a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6841a-105">DESCRIPTION</span></span>
<span data-ttu-id="6841a-106">**Get-AzSqlDatabase** cmdlet 'ı BIR Azure SQL veritabanı sunucusundan bir veya birden çok Azure SQL veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="6841a-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="6841a-107">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="6841a-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6841a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6841a-108">EXAMPLES</span></span>

### <span data-ttu-id="6841a-109">Örnek 1: sunucudaki tüm veritabanlarını alma</span><span class="sxs-lookup"><span data-stu-id="6841a-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : master
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="6841a-110">Bu komut, server01 adındaki sunucudaki tüm veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6841a-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="6841a-111">Örnek 2: sunucudaki bir veritabanını adıyla alma</span><span class="sxs-lookup"><span data-stu-id="6841a-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="6841a-112">Bu komut, server01 adındaki bir Database02 adlı sunucudan gelen veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="6841a-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="6841a-113">Örnek 3: filtreleme kullanarak sunucudaki tüm veritabanlarını alma</span><span class="sxs-lookup"><span data-stu-id="6841a-113">Example 3: Get all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database*"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="6841a-114">Bu komut, sunucudaki "veritabanı" ile başlayan tüm veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6841a-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="6841a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6841a-115">PARAMETERS</span></span>

### <span data-ttu-id="6841a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6841a-116">-DatabaseName</span></span>
<span data-ttu-id="6841a-117">Alınacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6841a-117">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6841a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6841a-118">-DefaultProfile</span></span>
<span data-ttu-id="6841a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6841a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6841a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6841a-120">-ResourceGroupName</span></span>
<span data-ttu-id="6841a-121">Veritabanı sunucusunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6841a-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="6841a-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6841a-122">-ServerName</span></span>
<span data-ttu-id="6841a-123">Veritabanının atandığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6841a-123">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="6841a-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="6841a-124">-Confirm</span></span>
<span data-ttu-id="6841a-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6841a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6841a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6841a-126">-WhatIf</span></span>
<span data-ttu-id="6841a-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6841a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6841a-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6841a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6841a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6841a-129">CommonParameters</span></span>
<span data-ttu-id="6841a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6841a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6841a-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6841a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6841a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6841a-132">INPUTS</span></span>

### <span data-ttu-id="6841a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6841a-133">System.String</span></span>

## <span data-ttu-id="6841a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6841a-134">OUTPUTS</span></span>

### <span data-ttu-id="6841a-135">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="6841a-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="6841a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6841a-136">NOTES</span></span>

## <span data-ttu-id="6841a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6841a-137">RELATED LINKS</span></span>

[<span data-ttu-id="6841a-138">Yeni-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6841a-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="6841a-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6841a-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="6841a-140">Özgeçmiş-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6841a-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="6841a-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6841a-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="6841a-142">Askıya al-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6841a-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)


