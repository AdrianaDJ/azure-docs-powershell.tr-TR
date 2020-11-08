---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8090ee9cf6ec251668dbeadba6b18a7cde4898c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097044"
---
# <span data-ttu-id="a1568-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="a1568-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="a1568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1568-102">SYNOPSIS</span></span>
<span data-ttu-id="a1568-103">Veritabanının Gelişmiş tehdit koruması ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a1568-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="a1568-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1568-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1568-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1568-105">DESCRIPTION</span></span>
<span data-ttu-id="a1568-106">**Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet 'i, BIR Azure SQL veritabanının Gelişmiş tehdit koruması ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a1568-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="a1568-107">Bu cmdlet 'i kullanmak için, bu cmdlet 'in ayarları aldığı veritabanını tanımlamak üzere *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="a1568-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="a1568-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1568-108">EXAMPLES</span></span>

### <span data-ttu-id="a1568-109">Örnek 1: veritabanı için Gelişmiş tehdit koruması ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="a1568-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="a1568-110">Bu komut, Database01 adlı bir veritabanı için Gelişmiş tehdit koruması ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a1568-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="a1568-111">Veritabanı, server01 adlı sunucuda, kaynak grubuna atanmış ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a1568-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="a1568-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1568-112">PARAMETERS</span></span>

### <span data-ttu-id="a1568-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a1568-113">-DatabaseName</span></span>
<span data-ttu-id="a1568-114">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1568-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="a1568-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1568-115">-DefaultProfile</span></span>
<span data-ttu-id="a1568-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a1568-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1568-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1568-117">-ResourceGroupName</span></span>
<span data-ttu-id="a1568-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1568-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a1568-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a1568-119">-ServerName</span></span>
<span data-ttu-id="a1568-120">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1568-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="a1568-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="a1568-121">-Confirm</span></span>
<span data-ttu-id="a1568-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a1568-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1568-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1568-123">-WhatIf</span></span>
<span data-ttu-id="a1568-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1568-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1568-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a1568-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1568-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1568-126">CommonParameters</span></span>
<span data-ttu-id="a1568-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1568-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1568-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a1568-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1568-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1568-129">INPUTS</span></span>

### <span data-ttu-id="a1568-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a1568-130">System.String</span></span>

## <span data-ttu-id="a1568-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1568-131">OUTPUTS</span></span>

### <span data-ttu-id="a1568-132">Microsoft. Azure. Commands. Sql. ThreatDetection. model. DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="a1568-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="a1568-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1568-133">NOTES</span></span>

## <span data-ttu-id="a1568-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1568-134">RELATED LINKS</span></span>

[<span data-ttu-id="a1568-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="a1568-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)



