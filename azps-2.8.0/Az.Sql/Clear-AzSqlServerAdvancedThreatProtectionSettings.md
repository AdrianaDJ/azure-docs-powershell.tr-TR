---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 215ab742a91bc70c51860950acedb3449966bda2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932382"
---
# <span data-ttu-id="4e8c1-101">Clear-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="4e8c1-101">Clear-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="4e8c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="4e8c1-103">Gelişmiş tehdit koruması ayarlarını sunucudan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4e8c1-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="4e8c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e8c1-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSettings [-PassThru] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e8c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e8c1-105">DESCRIPTION</span></span>
<span data-ttu-id="4e8c1-106">Clear-AzSqlServerAdvancedThreatProtectionSettings cmdlet 'i Azure SQL Server 'dan Gelişmiş tehdit koruması ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4e8c1-106">The Clear-AzSqlServerAdvancedThreatProtectionSettings cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="4e8c1-107">Bu cmdlet 'i kullanmak için, bu cmdlet 'in ayarları kaldırdığı sunucuyu belirlemek için ResourceGroupName ve ServerName parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="4e8c1-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="4e8c1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e8c1-108">EXAMPLES</span></span>

### <span data-ttu-id="4e8c1-109">Örnek 1: veritabanı için Gelişmiş tehdit koruması ayarlarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="4e8c1-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="4e8c1-110">Bu komut, server01 adındaki Gelişmiş tehdit koruması ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4e8c1-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="4e8c1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e8c1-111">PARAMETERS</span></span>

### <span data-ttu-id="4e8c1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e8c1-112">-DefaultProfile</span></span>
<span data-ttu-id="4e8c1-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4e8c1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e8c1-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4e8c1-114">-PassThru</span></span>
<span data-ttu-id="4e8c1-115">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="4e8c1-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4e8c1-116">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4e8c1-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4e8c1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e8c1-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e8c1-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e8c1-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="4e8c1-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4e8c1-119">-ServerName</span></span>
<span data-ttu-id="4e8c1-120">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e8c1-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="4e8c1-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="4e8c1-121">-Confirm</span></span>
<span data-ttu-id="4e8c1-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4e8c1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e8c1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e8c1-123">-WhatIf</span></span>
<span data-ttu-id="4e8c1-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4e8c1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e8c1-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4e8c1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e8c1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e8c1-126">CommonParameters</span></span>
<span data-ttu-id="4e8c1-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e8c1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e8c1-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e8c1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e8c1-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e8c1-129">INPUTS</span></span>

### <span data-ttu-id="4e8c1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4e8c1-130">System.String</span></span>

## <span data-ttu-id="4e8c1-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e8c1-131">OUTPUTS</span></span>

### <span data-ttu-id="4e8c1-132">Microsoft. Azure. Commands. Sql. ThreatDetection. model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="4e8c1-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="4e8c1-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e8c1-133">NOTES</span></span>

## <span data-ttu-id="4e8c1-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e8c1-134">RELATED LINKS</span></span>

[<span data-ttu-id="4e8c1-135">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="4e8c1-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
