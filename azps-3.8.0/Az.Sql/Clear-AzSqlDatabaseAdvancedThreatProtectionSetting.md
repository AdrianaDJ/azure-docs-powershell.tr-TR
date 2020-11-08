---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 7bdfb6ef415cdf5f3cac173730770307701b50bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103719"
---
# <span data-ttu-id="3ffad-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="3ffad-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="3ffad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ffad-102">SYNOPSIS</span></span>
<span data-ttu-id="3ffad-103">Veritabanından Gelişmiş tehdit koruması ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3ffad-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="3ffad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ffad-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ffad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ffad-105">DESCRIPTION</span></span>
<span data-ttu-id="3ffad-106">**Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet 'ı Azureazer SQL veritabanından Gelişmiş tehdit koruması ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3ffad-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="3ffad-107">Bu cmdlet 'i kullanmak için, bu cmdlet 'in ayarları kaldırdığı veritabanını belirlemek için *Resourcegroupname* ve *ServerName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="3ffad-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="3ffad-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ffad-108">EXAMPLES</span></span>

### <span data-ttu-id="3ffad-109">Örnek 1: veritabanı için Gelişmiş tehdit koruması ayarlarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3ffad-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="3ffad-110">Bu komut, server01 adındaki sunucudaki Database01 adındaki Gelişmiş tehdit koruması ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3ffad-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="3ffad-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ffad-111">PARAMETERS</span></span>

### <span data-ttu-id="3ffad-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3ffad-112">-DatabaseName</span></span>
<span data-ttu-id="3ffad-113">Gelişmiş tehdit koruması ayarlarının kaldırılması gereken veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ffad-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="3ffad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ffad-114">-DefaultProfile</span></span>
<span data-ttu-id="3ffad-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3ffad-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ffad-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3ffad-116">-PassThru</span></span>
<span data-ttu-id="3ffad-117">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="3ffad-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3ffad-118">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3ffad-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ffad-119">-ResourceGroupName</span></span>
<span data-ttu-id="3ffad-120">Sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ffad-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="3ffad-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3ffad-121">-ServerName</span></span>
<span data-ttu-id="3ffad-122">Veritabanının çalıştığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ffad-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="3ffad-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="3ffad-123">-Confirm</span></span>
<span data-ttu-id="3ffad-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3ffad-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ffad-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ffad-125">-WhatIf</span></span>
<span data-ttu-id="3ffad-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ffad-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ffad-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3ffad-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ffad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ffad-128">CommonParameters</span></span>
<span data-ttu-id="3ffad-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ffad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ffad-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3ffad-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ffad-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ffad-131">INPUTS</span></span>

### <span data-ttu-id="3ffad-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3ffad-132">System.String</span></span>

## <span data-ttu-id="3ffad-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ffad-133">OUTPUTS</span></span>

### <span data-ttu-id="3ffad-134">Microsoft. Azure. Commands. Sql. ThreatDetection. model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="3ffad-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="3ffad-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ffad-135">NOTES</span></span>

## <span data-ttu-id="3ffad-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ffad-136">RELATED LINKS</span></span>

[<span data-ttu-id="3ffad-137">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="3ffad-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


