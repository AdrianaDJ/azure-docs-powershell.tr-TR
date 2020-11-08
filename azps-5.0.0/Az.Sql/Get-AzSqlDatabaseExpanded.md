---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: 18d387aeb8ca9e777af0767ce407e373fc2adf09
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275201"
---
# <span data-ttu-id="7cc70-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="7cc70-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="7cc70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cc70-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc70-103">Bir veritabanını ve genişletilmiş özellik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="7cc70-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="7cc70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7cc70-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cc70-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7cc70-105">DESCRIPTION</span></span>
<span data-ttu-id="7cc70-106">**Get-Azsqldatabasegenişletilen** cmdlet 'i bir veritabanını ve genişletilmiş özellik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="7cc70-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="7cc70-107">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="7cc70-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7cc70-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7cc70-108">EXAMPLES</span></span>

### <span data-ttu-id="7cc70-109">Örnek 1: hizmet katmanı Danışmanı bilgilerini içeren veritabanı nesnesini alma</span><span class="sxs-lookup"><span data-stu-id="7cc70-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="7cc70-110">Bu komut, hizmet katmanı Danışmanı bilgilerini içeren genişletilmiş özellikleri içeren veritabanını döndürür.</span><span class="sxs-lookup"><span data-stu-id="7cc70-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="7cc70-111">Örnek 2: filtreleme kullanarak veritabanı nesnelerini listeleme</span><span class="sxs-lookup"><span data-stu-id="7cc70-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="7cc70-112">Bu komut, server01 'da "veritabanı" ile başlayan tüm veritabanları için genişletilmiş veritabanı nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="7cc70-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="7cc70-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7cc70-113">PARAMETERS</span></span>

### <span data-ttu-id="7cc70-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7cc70-114">-DatabaseName</span></span>
<span data-ttu-id="7cc70-115">Alınacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cc70-115">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="7cc70-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc70-116">-DefaultProfile</span></span>
<span data-ttu-id="7cc70-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7cc70-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cc70-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cc70-118">-ResourceGroupName</span></span>
<span data-ttu-id="7cc70-119">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cc70-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7cc70-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7cc70-120">-ServerName</span></span>
<span data-ttu-id="7cc70-121">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cc70-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="7cc70-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="7cc70-122">-Confirm</span></span>
<span data-ttu-id="7cc70-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7cc70-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cc70-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cc70-124">-WhatIf</span></span>
<span data-ttu-id="7cc70-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cc70-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cc70-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7cc70-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cc70-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc70-127">CommonParameters</span></span>
<span data-ttu-id="7cc70-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7cc70-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc70-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7cc70-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc70-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7cc70-130">INPUTS</span></span>

### <span data-ttu-id="7cc70-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7cc70-131">System.String</span></span>

## <span data-ttu-id="7cc70-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7cc70-132">OUTPUTS</span></span>

### <span data-ttu-id="7cc70-133">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodelexpanded</span><span class="sxs-lookup"><span data-stu-id="7cc70-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="7cc70-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7cc70-134">NOTES</span></span>

## <span data-ttu-id="7cc70-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7cc70-135">RELATED LINKS</span></span>

[<span data-ttu-id="7cc70-136">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="7cc70-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
