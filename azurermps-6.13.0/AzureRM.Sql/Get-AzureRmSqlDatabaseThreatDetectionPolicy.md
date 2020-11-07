---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 483c58a980abc67a261ef5795b2bde4d91224e66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592722"
---
# <span data-ttu-id="be752-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="be752-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="be752-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be752-102">SYNOPSIS</span></span>
<span data-ttu-id="be752-103">Bir veritabanı için tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="be752-103">Gets the threat detection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be752-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be752-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be752-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="be752-105">DESCRIPTION</span></span>
<span data-ttu-id="be752-106">**Get-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet 'ı BIR Azure SQL veritabanının tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="be752-106">The **Get-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="be752-107">Bu cmdlet 'i kullanmak için, bu cmdlet 'in ilkeyi aldığı veritabanını tanımlamak üzere *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="be752-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="be752-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be752-108">EXAMPLES</span></span>

### <span data-ttu-id="be752-109">Örnek 1: veritabanı için tehdit algılama ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="be752-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="be752-110">Bu komut, Database01 adlı bir veritabanı için tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="be752-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="be752-111">Veritabanı, server01 adlı sunucuda, kaynak grubuna atanmış ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="be752-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="be752-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be752-112">PARAMETERS</span></span>

### <span data-ttu-id="be752-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="be752-113">-DatabaseName</span></span>
<span data-ttu-id="be752-114">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be752-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="be752-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be752-115">-DefaultProfile</span></span>
<span data-ttu-id="be752-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="be752-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be752-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be752-117">-ResourceGroupName</span></span>
<span data-ttu-id="be752-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be752-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="be752-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="be752-119">-ServerName</span></span>
<span data-ttu-id="be752-120">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be752-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="be752-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="be752-121">-Confirm</span></span>
<span data-ttu-id="be752-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be752-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be752-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be752-123">-WhatIf</span></span>
<span data-ttu-id="be752-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="be752-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be752-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="be752-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be752-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be752-126">CommonParameters</span></span>
<span data-ttu-id="be752-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be752-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be752-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be752-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be752-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be752-129">INPUTS</span></span>

### <span data-ttu-id="be752-130">System. String</span><span class="sxs-lookup"><span data-stu-id="be752-130">System.String</span></span>

## <span data-ttu-id="be752-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be752-131">OUTPUTS</span></span>

### <span data-ttu-id="be752-132">Microsoft. Azure. Commands. Sql. ThreatDetection. model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="be752-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="be752-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be752-133">NOTES</span></span>

## <span data-ttu-id="be752-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be752-134">RELATED LINKS</span></span>

[<span data-ttu-id="be752-135">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="be752-135">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)


