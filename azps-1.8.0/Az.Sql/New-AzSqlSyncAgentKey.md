---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: 4b04fe3a27178ce5228f8e3fe2a397728a432b6b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758872"
---
# <span data-ttu-id="210d6-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="210d6-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="210d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="210d6-102">SYNOPSIS</span></span>
<span data-ttu-id="210d6-103">Azure SQL eşitleme Aracısı anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="210d6-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="210d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="210d6-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="210d6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="210d6-105">DESCRIPTION</span></span>
<span data-ttu-id="210d6-106">**New-AzSqlSyncAgentKey** cmdlet 'ı Azure SQL eşitleme Aracısı anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="210d6-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="210d6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="210d6-107">EXAMPLES</span></span>

### <span data-ttu-id="210d6-108">Örnek 1: Azure SQL eşitleme Aracısı için eşitleme Aracısı anahtarı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="210d6-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="210d6-109">Bu komut, Azure SQL eşitleme Aracısı için eşitleme Aracısı anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="210d6-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="210d6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="210d6-110">PARAMETERS</span></span>

### <span data-ttu-id="210d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="210d6-111">-DefaultProfile</span></span>
<span data-ttu-id="210d6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="210d6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="210d6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="210d6-113">-ResourceGroupName</span></span>
<span data-ttu-id="210d6-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="210d6-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="210d6-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="210d6-115">-ServerName</span></span>
<span data-ttu-id="210d6-116">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="210d6-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="210d6-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="210d6-117">-SyncAgentName</span></span>
<span data-ttu-id="210d6-118">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="210d6-118">The sync agent name.</span></span>

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

### <span data-ttu-id="210d6-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="210d6-119">-Confirm</span></span>
<span data-ttu-id="210d6-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="210d6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="210d6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="210d6-121">-WhatIf</span></span>
<span data-ttu-id="210d6-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="210d6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="210d6-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="210d6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="210d6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="210d6-124">CommonParameters</span></span>
<span data-ttu-id="210d6-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="210d6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="210d6-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="210d6-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="210d6-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="210d6-127">INPUTS</span></span>

### <span data-ttu-id="210d6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="210d6-128">System.String</span></span>

## <span data-ttu-id="210d6-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="210d6-129">OUTPUTS</span></span>

### <span data-ttu-id="210d6-130">Microsoft. Azure. Commands. Sql. DataSync. model. azures, Syncagentkeymodel</span><span class="sxs-lookup"><span data-stu-id="210d6-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="210d6-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="210d6-131">NOTES</span></span>

## <span data-ttu-id="210d6-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="210d6-132">RELATED LINKS</span></span>
