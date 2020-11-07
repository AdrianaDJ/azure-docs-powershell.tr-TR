---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: f8d01165825c63ece34779f58cb94a3f8e0af40c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758932"
---
# <span data-ttu-id="72caf-101">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="72caf-101">Get-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="72caf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72caf-102">SYNOPSIS</span></span>
<span data-ttu-id="72caf-103">Sunucu için tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="72caf-103">Gets the threat detection policy for a server.</span></span>

## <span data-ttu-id="72caf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72caf-104">SYNTAX</span></span>

```
Get-AzSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72caf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72caf-105">DESCRIPTION</span></span>
<span data-ttu-id="72caf-106">**Get-AzSqlServerThreatDetectionPolicy** cmdlet 'ı BIR Azure SQL Server 'ın tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="72caf-106">The **Get-AzSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="72caf-107">Bu cmdlet 'i kullanmak için, bu cmdlet 'in ilkeyi aldığı sunucuyu tanımlayacak *Resourcegroupname* ve *ServerName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="72caf-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="72caf-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72caf-108">EXAMPLES</span></span>

### <span data-ttu-id="72caf-109">Örnek 1: sunucunun tehdit algılama ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="72caf-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="72caf-110">Bu komut, server01 adlı bir sunucuda tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="72caf-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="72caf-111">Sunucu, ResourceGroup11 kaynak grubuna atanır.</span><span class="sxs-lookup"><span data-stu-id="72caf-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="72caf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72caf-112">PARAMETERS</span></span>

### <span data-ttu-id="72caf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72caf-113">-DefaultProfile</span></span>
<span data-ttu-id="72caf-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="72caf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72caf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72caf-115">-ResourceGroupName</span></span>
<span data-ttu-id="72caf-116">Sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72caf-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="72caf-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72caf-117">-ServerName</span></span>
<span data-ttu-id="72caf-118">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72caf-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="72caf-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="72caf-119">-Confirm</span></span>
<span data-ttu-id="72caf-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72caf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72caf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72caf-121">-WhatIf</span></span>
<span data-ttu-id="72caf-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72caf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72caf-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72caf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72caf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72caf-124">CommonParameters</span></span>
<span data-ttu-id="72caf-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72caf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72caf-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="72caf-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72caf-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72caf-127">INPUTS</span></span>

### <span data-ttu-id="72caf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="72caf-128">System.String</span></span>

## <span data-ttu-id="72caf-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72caf-129">OUTPUTS</span></span>

### <span data-ttu-id="72caf-130">Microsoft. Azure. Commands. Sql. ThreatDetection. model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="72caf-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="72caf-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72caf-131">NOTES</span></span>

## <span data-ttu-id="72caf-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72caf-132">RELATED LINKS</span></span>

[<span data-ttu-id="72caf-133">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="72caf-133">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="72caf-134">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="72caf-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


