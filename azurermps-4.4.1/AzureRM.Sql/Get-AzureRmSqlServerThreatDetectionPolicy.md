---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 1cb77a435ee951e2e7fe4bc7401e7e4385557eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592992"
---
# <span data-ttu-id="8554f-101">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8554f-101">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="8554f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8554f-102">SYNOPSIS</span></span>
<span data-ttu-id="8554f-103">Sunucu için tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="8554f-103">Gets the threat detection policy for a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8554f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8554f-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8554f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8554f-105">DESCRIPTION</span></span>
<span data-ttu-id="8554f-106">**Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet 'ı BIR Azure SQL Server 'ın tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="8554f-106">The **Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="8554f-107">Bu cmdlet 'i kullanmak için, bu cmdlet 'in ilkeyi aldığı sunucuyu tanımlayacak *Resourcegroupname* ve *ServerName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8554f-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="8554f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8554f-108">EXAMPLES</span></span>

### <span data-ttu-id="8554f-109">Örnek 1: sunucunun tehdit algılama ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="8554f-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="8554f-110">Bu komut, server01 adlı bir sunucuda tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="8554f-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="8554f-111">Sunucu, ResourceGroup11 kaynak grubuna atanır.</span><span class="sxs-lookup"><span data-stu-id="8554f-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="8554f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8554f-112">PARAMETERS</span></span>

### <span data-ttu-id="8554f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8554f-113">-ResourceGroupName</span></span>
<span data-ttu-id="8554f-114">Sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8554f-114">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="8554f-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8554f-115">-ServerName</span></span>
<span data-ttu-id="8554f-116">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8554f-116">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="8554f-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="8554f-117">-Confirm</span></span>
<span data-ttu-id="8554f-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8554f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8554f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8554f-119">-WhatIf</span></span>
<span data-ttu-id="8554f-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8554f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8554f-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8554f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8554f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8554f-122">-DefaultProfile</span></span>
<span data-ttu-id="8554f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8554f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8554f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8554f-124">CommonParameters</span></span>
<span data-ttu-id="8554f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8554f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8554f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8554f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8554f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8554f-127">INPUTS</span></span>

## <span data-ttu-id="8554f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8554f-128">OUTPUTS</span></span>

### <span data-ttu-id="8554f-129">Microsoft. Azure. Commands. Sql. ThreatDetection. model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="8554f-129">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="8554f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8554f-130">NOTES</span></span>

## <span data-ttu-id="8554f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8554f-131">RELATED LINKS</span></span>

[<span data-ttu-id="8554f-132">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8554f-132">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="8554f-133">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="8554f-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


