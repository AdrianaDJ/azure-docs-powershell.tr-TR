---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277002"
---
# <span data-ttu-id="cfe79-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="cfe79-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="cfe79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfe79-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe79-103">Gelişmiş tehdit koruması ayarlarını sunucudan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cfe79-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="cfe79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cfe79-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfe79-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cfe79-105">DESCRIPTION</span></span>
<span data-ttu-id="cfe79-106">Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet 'i Azure SQL Server 'dan Gelişmiş tehdit koruması ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cfe79-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="cfe79-107">Bu cmdlet 'i kullanmak için, bu cmdlet 'in ayarları kaldırdığı sunucuyu belirlemek için ResourceGroupName ve ServerName parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="cfe79-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="cfe79-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cfe79-108">EXAMPLES</span></span>

### <span data-ttu-id="cfe79-109">Örnek 1: veritabanı için Gelişmiş tehdit koruması ayarlarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="cfe79-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="cfe79-110">Bu komut, server01 adındaki Gelişmiş tehdit koruması ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cfe79-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="cfe79-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cfe79-111">PARAMETERS</span></span>

### <span data-ttu-id="cfe79-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe79-112">-DefaultProfile</span></span>
<span data-ttu-id="cfe79-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cfe79-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfe79-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cfe79-114">-PassThru</span></span>
<span data-ttu-id="cfe79-115">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="cfe79-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cfe79-116">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="cfe79-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cfe79-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfe79-117">-ResourceGroupName</span></span>
<span data-ttu-id="cfe79-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe79-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="cfe79-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cfe79-119">-ServerName</span></span>
<span data-ttu-id="cfe79-120">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe79-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="cfe79-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="cfe79-121">-Confirm</span></span>
<span data-ttu-id="cfe79-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cfe79-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfe79-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfe79-123">-WhatIf</span></span>
<span data-ttu-id="cfe79-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cfe79-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfe79-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cfe79-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfe79-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe79-126">CommonParameters</span></span>
<span data-ttu-id="cfe79-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cfe79-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe79-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cfe79-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe79-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cfe79-129">INPUTS</span></span>

### <span data-ttu-id="cfe79-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cfe79-130">System.String</span></span>

## <span data-ttu-id="cfe79-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cfe79-131">OUTPUTS</span></span>

### <span data-ttu-id="cfe79-132">Microsoft. Azure. Commands. Sql. ThreatDetection. model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="cfe79-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="cfe79-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cfe79-133">NOTES</span></span>

## <span data-ttu-id="cfe79-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cfe79-134">RELATED LINKS</span></span>

[<span data-ttu-id="cfe79-135">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="cfe79-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

