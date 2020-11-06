---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
ms.openlocfilehash: cb4ca947d9f87cd6a0d3b4cdf476cf0176db2c3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587129"
---
# <span data-ttu-id="2dfe1-101">New-AzureRmSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="2dfe1-101">New-AzureRmSqlSyncAgentKey</span></span>

## <span data-ttu-id="2dfe1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dfe1-102">SYNOPSIS</span></span>
<span data-ttu-id="2dfe1-103">Azure SQL eşitleme Aracısı anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-103">Creates an Azure SQL Sync Agent Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dfe1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2dfe1-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dfe1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2dfe1-105">DESCRIPTION</span></span>
<span data-ttu-id="2dfe1-106">**Yeni-AzureRmSqlSyncAgentKey** cmdlet 'ı Azure SQL eşitleme Aracısı anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-106">The **New-AzureRmSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="2dfe1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2dfe1-107">EXAMPLES</span></span>

### <span data-ttu-id="2dfe1-108">Örnek 1: Azure SQL eşitleme Aracısı için eşitleme Aracısı anahtarı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="2dfe1-109">Bu komut, Azure SQL eşitleme Aracısı için eşitleme Aracısı anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="2dfe1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2dfe1-110">PARAMETERS</span></span>

### <span data-ttu-id="2dfe1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dfe1-111">-DefaultProfile</span></span>
<span data-ttu-id="2dfe1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2dfe1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dfe1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dfe1-113">-ResourceGroupName</span></span>
<span data-ttu-id="2dfe1-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="2dfe1-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2dfe1-115">-ServerName</span></span>
<span data-ttu-id="2dfe1-116">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="2dfe1-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="2dfe1-117">-SyncAgentName</span></span>
<span data-ttu-id="2dfe1-118">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-118">The sync agent name.</span></span>

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

### <span data-ttu-id="2dfe1-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="2dfe1-119">-Confirm</span></span>
<span data-ttu-id="2dfe1-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dfe1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dfe1-121">-WhatIf</span></span>
<span data-ttu-id="2dfe1-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dfe1-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dfe1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dfe1-124">CommonParameters</span></span>
<span data-ttu-id="2dfe1-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dfe1-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dfe1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dfe1-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2dfe1-127">INPUTS</span></span>

### <span data-ttu-id="2dfe1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2dfe1-128">System.String</span></span>

## <span data-ttu-id="2dfe1-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2dfe1-129">OUTPUTS</span></span>

### <span data-ttu-id="2dfe1-130">Microsoft. Azure. Commands. Sql. DataSync. model. azures, Syncagentkeymodel</span><span class="sxs-lookup"><span data-stu-id="2dfe1-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="2dfe1-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2dfe1-131">NOTES</span></span>

## <span data-ttu-id="2dfe1-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2dfe1-132">RELATED LINKS</span></span>
