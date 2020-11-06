---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
ms.openlocfilehash: 56254dc295b650012cdff321f4f6e77054614186
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594551"
---
# <span data-ttu-id="ddf77-101">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="ddf77-101">Get-AzureRmSqlDatabaseExpanded</span></span>

## <span data-ttu-id="ddf77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddf77-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf77-103">Bir veritabanını ve genişletilmiş özellik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="ddf77-103">Gets a database and its expanded property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddf77-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddf77-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddf77-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddf77-105">DESCRIPTION</span></span>
<span data-ttu-id="ddf77-106">**Get-Azurermsqldatabasegenişletilen** cmdlet 'i bir veritabanını ve genişletilmiş özellik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="ddf77-106">The **Get-AzureRmSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>

<span data-ttu-id="ddf77-107">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="ddf77-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ddf77-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddf77-108">EXAMPLES</span></span>

### <span data-ttu-id="ddf77-109">Örnek 1: hizmet katmanı Danışmanı bilgilerini içeren veritabanı nesnesini alma</span><span class="sxs-lookup"><span data-stu-id="ddf77-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\>Get-AzureSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ddf77-110">Bu komut, hizmet katmanı Danışmanı bilgilerini içeren genişletilmiş özellikleri içeren veritabanını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ddf77-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

## <span data-ttu-id="ddf77-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddf77-111">PARAMETERS</span></span>

### <span data-ttu-id="ddf77-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ddf77-112">-DatabaseName</span></span>
<span data-ttu-id="ddf77-113">Alınacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddf77-113">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="ddf77-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf77-114">-ResourceGroupName</span></span>
<span data-ttu-id="ddf77-115">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddf77-115">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ddf77-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ddf77-116">-ServerName</span></span>
<span data-ttu-id="ddf77-117">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddf77-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ddf77-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="ddf77-118">-Confirm</span></span>
<span data-ttu-id="ddf77-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ddf77-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddf77-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddf77-120">-WhatIf</span></span>
<span data-ttu-id="ddf77-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddf77-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddf77-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ddf77-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddf77-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf77-123">-DefaultProfile</span></span>
<span data-ttu-id="ddf77-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ddf77-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddf77-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf77-125">CommonParameters</span></span>
<span data-ttu-id="ddf77-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddf77-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf77-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddf77-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf77-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddf77-128">INPUTS</span></span>

## <span data-ttu-id="ddf77-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddf77-129">OUTPUTS</span></span>

## <span data-ttu-id="ddf77-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddf77-130">NOTES</span></span>

## <span data-ttu-id="ddf77-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddf77-131">RELATED LINKS</span></span>

[<span data-ttu-id="ddf77-132">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="ddf77-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
