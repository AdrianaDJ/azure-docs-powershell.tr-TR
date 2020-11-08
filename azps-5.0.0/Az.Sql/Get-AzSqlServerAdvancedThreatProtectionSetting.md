---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 94963c8c5d61c91e2d53cdf7b12cc333acc566a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279435"
---
# <span data-ttu-id="72b83-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="72b83-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="72b83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72b83-102">SYNOPSIS</span></span>
<span data-ttu-id="72b83-103">Sunucunun Gelişmiş tehdit koruması ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="72b83-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="72b83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72b83-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72b83-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72b83-105">DESCRIPTION</span></span>
<span data-ttu-id="72b83-106">**Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet 'i, BIR Azure SQL Server 'ın Gelişmiş tehdit koruması ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="72b83-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="72b83-107">Bu cmdlet 'i kullanmak için, bu cmdlet 'in ayarları aldığı sunucuyu tanımlayacak *Resourcegroupname* ve *ServerName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="72b83-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="72b83-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72b83-108">EXAMPLES</span></span>

### <span data-ttu-id="72b83-109">Örnek 1: sunucunun Gelişmiş tehdit koruması ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="72b83-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="72b83-110">Bu komut, server01 adlı bir sunucunun Gelişmiş tehdit koruması ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="72b83-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="72b83-111">Sunucu, ResourceGroup11 kaynak grubuna atanır.</span><span class="sxs-lookup"><span data-stu-id="72b83-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="72b83-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72b83-112">PARAMETERS</span></span>

### <span data-ttu-id="72b83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b83-113">-DefaultProfile</span></span>
<span data-ttu-id="72b83-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="72b83-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72b83-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72b83-115">-ResourceGroupName</span></span>
<span data-ttu-id="72b83-116">Sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72b83-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="72b83-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72b83-117">-ServerName</span></span>
<span data-ttu-id="72b83-118">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72b83-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="72b83-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="72b83-119">-Confirm</span></span>
<span data-ttu-id="72b83-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72b83-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72b83-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72b83-121">-WhatIf</span></span>
<span data-ttu-id="72b83-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72b83-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72b83-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72b83-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72b83-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b83-124">CommonParameters</span></span>
<span data-ttu-id="72b83-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72b83-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b83-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="72b83-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b83-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72b83-127">INPUTS</span></span>

### <span data-ttu-id="72b83-128">System. String</span><span class="sxs-lookup"><span data-stu-id="72b83-128">System.String</span></span>

## <span data-ttu-id="72b83-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72b83-129">OUTPUTS</span></span>

### <span data-ttu-id="72b83-130">Microsoft. Azure. Commands. Sql. ThreatDetection. model. ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="72b83-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="72b83-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72b83-131">NOTES</span></span>

## <span data-ttu-id="72b83-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72b83-132">RELATED LINKS</span></span>

[<span data-ttu-id="72b83-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="72b83-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="72b83-134">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="72b83-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


