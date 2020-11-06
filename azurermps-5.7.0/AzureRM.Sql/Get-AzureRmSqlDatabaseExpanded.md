---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
ms.openlocfilehash: 472e8e7a2f0919115686764136b6b40f5e1da913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589664"
---
# <span data-ttu-id="76d18-101">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="76d18-101">Get-AzureRmSqlDatabaseExpanded</span></span>

## <span data-ttu-id="76d18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76d18-102">SYNOPSIS</span></span>
<span data-ttu-id="76d18-103">Bir veritabanını ve genişletilmiş özellik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="76d18-103">Gets a database and its expanded property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76d18-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76d18-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76d18-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76d18-105">DESCRIPTION</span></span>
<span data-ttu-id="76d18-106">**Get-Azurermsqldatabasegenişletilen** cmdlet 'i bir veritabanını ve genişletilmiş özellik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="76d18-106">The **Get-AzureRmSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>

<span data-ttu-id="76d18-107">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="76d18-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="76d18-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76d18-108">EXAMPLES</span></span>

### <span data-ttu-id="76d18-109">Örnek 1: hizmet katmanı Danışmanı bilgilerini içeren veritabanı nesnesini alma</span><span class="sxs-lookup"><span data-stu-id="76d18-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\>Get-AzureSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="76d18-110">Bu komut, hizmet katmanı Danışmanı bilgilerini içeren genişletilmiş özellikleri içeren veritabanını döndürür.</span><span class="sxs-lookup"><span data-stu-id="76d18-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

## <span data-ttu-id="76d18-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76d18-111">PARAMETERS</span></span>

### <span data-ttu-id="76d18-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="76d18-112">-DatabaseName</span></span>
<span data-ttu-id="76d18-113">Alınacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76d18-113">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="76d18-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d18-114">-DefaultProfile</span></span>
<span data-ttu-id="76d18-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="76d18-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76d18-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d18-116">-ResourceGroupName</span></span>
<span data-ttu-id="76d18-117">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76d18-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="76d18-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="76d18-118">-ServerName</span></span>
<span data-ttu-id="76d18-119">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76d18-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="76d18-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="76d18-120">-Confirm</span></span>
<span data-ttu-id="76d18-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="76d18-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76d18-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76d18-122">-WhatIf</span></span>
<span data-ttu-id="76d18-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="76d18-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76d18-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="76d18-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76d18-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d18-125">CommonParameters</span></span>
<span data-ttu-id="76d18-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76d18-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d18-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76d18-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d18-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76d18-128">INPUTS</span></span>

### <span data-ttu-id="76d18-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="76d18-129">None</span></span>
<span data-ttu-id="76d18-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="76d18-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76d18-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76d18-131">OUTPUTS</span></span>

## <span data-ttu-id="76d18-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76d18-132">NOTES</span></span>

## <span data-ttu-id="76d18-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76d18-133">RELATED LINKS</span></span>

[<span data-ttu-id="76d18-134">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="76d18-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
