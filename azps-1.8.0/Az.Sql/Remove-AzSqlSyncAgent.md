---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: 5adb6d79904b617b0ddbeaae28c9c7860c028fb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758820"
---
# <span data-ttu-id="e6f67-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e6f67-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="e6f67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6f67-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f67-103">Azure SQL eşitleme aracısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e6f67-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="e6f67-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6f67-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6f67-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6f67-105">DESCRIPTION</span></span>
<span data-ttu-id="e6f67-106">**Remove-AzSqlSyncAgent** cmdlet 'ı BIR Azure SQL eşitleme aracısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e6f67-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="e6f67-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6f67-107">EXAMPLES</span></span>

### <span data-ttu-id="e6f67-108">Örnek 1: eşitleme aracısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e6f67-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="e6f67-109">Bu komut, syncAgent01 adındaki Azure SQL eşitleme aracısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e6f67-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="e6f67-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6f67-110">PARAMETERS</span></span>

### <span data-ttu-id="e6f67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f67-111">-DefaultProfile</span></span>
<span data-ttu-id="e6f67-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e6f67-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6f67-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e6f67-113">-Force</span></span>
<span data-ttu-id="e6f67-114">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="e6f67-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e6f67-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e6f67-115">-Name</span></span>
<span data-ttu-id="e6f67-116">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="e6f67-116">The sync agent name.</span></span>

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

### <span data-ttu-id="e6f67-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e6f67-117">-PassThru</span></span>
<span data-ttu-id="e6f67-118">Kaldırılan eşitleme aracısının döndürülmesini Isteyip Istemediğinizi tanımlar</span><span class="sxs-lookup"><span data-stu-id="e6f67-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="e6f67-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f67-119">-ResourceGroupName</span></span>
<span data-ttu-id="e6f67-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e6f67-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6f67-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6f67-121">-ServerName</span></span>
<span data-ttu-id="e6f67-122">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="e6f67-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="e6f67-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="e6f67-123">-Confirm</span></span>
<span data-ttu-id="e6f67-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6f67-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f67-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f67-125">-WhatIf</span></span>
<span data-ttu-id="e6f67-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6f67-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6f67-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e6f67-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6f67-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f67-128">CommonParameters</span></span>
<span data-ttu-id="e6f67-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6f67-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f67-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e6f67-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f67-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6f67-131">INPUTS</span></span>

### <span data-ttu-id="e6f67-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e6f67-132">System.String</span></span>

## <span data-ttu-id="e6f67-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6f67-133">OUTPUTS</span></span>

### <span data-ttu-id="e6f67-134">Microsoft. Azure. Commands. Sql. DataSync. model. azureskalite syncagentı</span><span class="sxs-lookup"><span data-stu-id="e6f67-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="e6f67-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6f67-135">NOTES</span></span>

## <span data-ttu-id="e6f67-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6f67-136">RELATED LINKS</span></span>

[<span data-ttu-id="e6f67-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e6f67-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="e6f67-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e6f67-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

