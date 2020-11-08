---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098644"
---
# <span data-ttu-id="7bbd5-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7bbd5-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="7bbd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bbd5-102">SYNOPSIS</span></span>
<span data-ttu-id="7bbd5-103">Azure SQL eşitleme aracısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7bbd5-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="7bbd5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bbd5-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bbd5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bbd5-105">DESCRIPTION</span></span>
<span data-ttu-id="7bbd5-106">**Remove-AzSqlSyncAgent** cmdlet 'ı BIR Azure SQL eşitleme aracısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7bbd5-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="7bbd5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bbd5-107">EXAMPLES</span></span>

### <span data-ttu-id="7bbd5-108">Örnek 1: eşitleme aracısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7bbd5-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="7bbd5-109">Bu komut, syncAgent01 adındaki Azure SQL eşitleme aracısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7bbd5-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="7bbd5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bbd5-110">PARAMETERS</span></span>

### <span data-ttu-id="7bbd5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bbd5-111">-DefaultProfile</span></span>
<span data-ttu-id="7bbd5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7bbd5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bbd5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7bbd5-113">-Force</span></span>
<span data-ttu-id="7bbd5-114">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="7bbd5-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7bbd5-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7bbd5-115">-Name</span></span>
<span data-ttu-id="7bbd5-116">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="7bbd5-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bbd5-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7bbd5-117">-PassThru</span></span>
<span data-ttu-id="7bbd5-118">Kaldırılan eşitleme aracısının döndürülmesini Isteyip Istemediğinizi tanımlar</span><span class="sxs-lookup"><span data-stu-id="7bbd5-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="7bbd5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bbd5-119">-ResourceGroupName</span></span>
<span data-ttu-id="7bbd5-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7bbd5-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7bbd5-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7bbd5-121">-ServerName</span></span>
<span data-ttu-id="7bbd5-122">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="7bbd5-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="7bbd5-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="7bbd5-123">-Confirm</span></span>
<span data-ttu-id="7bbd5-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7bbd5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bbd5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bbd5-125">-WhatIf</span></span>
<span data-ttu-id="7bbd5-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7bbd5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bbd5-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7bbd5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bbd5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bbd5-128">CommonParameters</span></span>
<span data-ttu-id="7bbd5-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bbd5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bbd5-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7bbd5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bbd5-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bbd5-131">INPUTS</span></span>

### <span data-ttu-id="7bbd5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7bbd5-132">System.String</span></span>

## <span data-ttu-id="7bbd5-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bbd5-133">OUTPUTS</span></span>

### <span data-ttu-id="7bbd5-134">Microsoft. Azure. Commands. Sql. DataSync. model. azureskalite syncagentı</span><span class="sxs-lookup"><span data-stu-id="7bbd5-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="7bbd5-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bbd5-135">NOTES</span></span>

## <span data-ttu-id="7bbd5-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bbd5-136">RELATED LINKS</span></span>

[<span data-ttu-id="7bbd5-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7bbd5-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="7bbd5-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7bbd5-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

