---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 18117a109448ec219364ee6563191683a1fbc8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589956"
---
# <span data-ttu-id="1c3e4-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="1c3e4-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="1c3e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c3e4-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3e4-103">Bir Azure SQL Server 'ın denetim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="1c3e4-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c3e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c3e4-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c3e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c3e4-105">DESCRIPTION</span></span>
<span data-ttu-id="1c3e4-106">**Get-AzureRmSqlServerAuditing** cmdlet 'i, BIR Azure SQL Server 'ın blob denetim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="1c3e4-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="1c3e4-107">Veritabanını tanımlamak için *Resourcegroupname* ve *ServerName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="1c3e4-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="1c3e4-108">Bu cmdlet, belirtilen Azure SQL Server 'da tanımlanan Azure SQL veritabanları tarafından kullanılan bir ilkeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="1c3e4-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="1c3e4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c3e4-109">EXAMPLES</span></span>

### <span data-ttu-id="1c3e4-110">Örnek 1: Azure SQL Server 'ın denetim ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="1c3e4-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="1c3e4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c3e4-111">PARAMETERS</span></span>

### <span data-ttu-id="1c3e4-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c3e4-112">-ResourceGroupName</span></span>
<span data-ttu-id="1c3e4-113">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1c3e4-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="1c3e4-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1c3e4-114">-ServerName</span></span>
<span data-ttu-id="1c3e4-115">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="1c3e4-115">SQL server name.</span></span>

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

### <span data-ttu-id="1c3e4-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="1c3e4-116">-Confirm</span></span>
<span data-ttu-id="1c3e4-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1c3e4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c3e4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c3e4-118">-WhatIf</span></span>
<span data-ttu-id="1c3e4-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c3e4-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c3e4-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1c3e4-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c3e4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3e4-121">-DefaultProfile</span></span>
<span data-ttu-id="1c3e4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1c3e4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c3e4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3e4-123">CommonParameters</span></span>
<span data-ttu-id="1c3e4-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c3e4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3e4-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c3e4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3e4-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c3e4-126">INPUTS</span></span>

## <span data-ttu-id="1c3e4-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c3e4-127">OUTPUTS</span></span>

### <span data-ttu-id="1c3e4-128">Microsoft. Azure. Commands. Sql. Security. model. Serverblobobauditingsettingsmodel</span><span class="sxs-lookup"><span data-stu-id="1c3e4-128">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="1c3e4-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c3e4-129">NOTES</span></span>

## <span data-ttu-id="1c3e4-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c3e4-130">RELATED LINKS</span></span>

