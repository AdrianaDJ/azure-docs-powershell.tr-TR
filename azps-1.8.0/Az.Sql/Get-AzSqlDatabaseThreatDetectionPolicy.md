---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 6cb14b368bf7f190c30ff32fdec12576d3189204
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759011"
---
# <span data-ttu-id="195e2-101">Get-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="195e2-101">Get-AzSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="195e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="195e2-102">SYNOPSIS</span></span>
<span data-ttu-id="195e2-103">Bir veritabanı için tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="195e2-103">Gets the threat detection policy for a database.</span></span>

## <span data-ttu-id="195e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="195e2-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="195e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="195e2-105">DESCRIPTION</span></span>
<span data-ttu-id="195e2-106">**Get-AzSqlDatabaseThreatDetectionPolicy** cmdlet 'ı BIR Azure SQL veritabanının tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="195e2-106">The **Get-AzSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="195e2-107">Bu cmdlet 'i kullanmak için, bu cmdlet 'in ilkeyi aldığı veritabanını tanımlamak üzere *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="195e2-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="195e2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="195e2-108">EXAMPLES</span></span>

### <span data-ttu-id="195e2-109">Örnek 1: veritabanı için tehdit algılama ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="195e2-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="195e2-110">Bu komut, Database01 adlı bir veritabanı için tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="195e2-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="195e2-111">Veritabanı, server01 adlı sunucuda, kaynak grubuna atanmış ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="195e2-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="195e2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="195e2-112">PARAMETERS</span></span>

### <span data-ttu-id="195e2-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="195e2-113">-DatabaseName</span></span>
<span data-ttu-id="195e2-114">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="195e2-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="195e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="195e2-115">-DefaultProfile</span></span>
<span data-ttu-id="195e2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="195e2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="195e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="195e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="195e2-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="195e2-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="195e2-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="195e2-119">-ServerName</span></span>
<span data-ttu-id="195e2-120">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="195e2-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="195e2-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="195e2-121">-Confirm</span></span>
<span data-ttu-id="195e2-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="195e2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="195e2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="195e2-123">-WhatIf</span></span>
<span data-ttu-id="195e2-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="195e2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="195e2-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="195e2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="195e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195e2-126">CommonParameters</span></span>
<span data-ttu-id="195e2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="195e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195e2-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="195e2-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195e2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="195e2-129">INPUTS</span></span>

### <span data-ttu-id="195e2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="195e2-130">System.String</span></span>

## <span data-ttu-id="195e2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="195e2-131">OUTPUTS</span></span>

### <span data-ttu-id="195e2-132">Microsoft. Azure. Commands. Sql. ThreatDetection. model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="195e2-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="195e2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="195e2-133">NOTES</span></span>

## <span data-ttu-id="195e2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="195e2-134">RELATED LINKS</span></span>

[<span data-ttu-id="195e2-135">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="195e2-135">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)



