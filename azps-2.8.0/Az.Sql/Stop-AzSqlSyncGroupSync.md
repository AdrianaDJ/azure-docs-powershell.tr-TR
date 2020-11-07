---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: e7c6dc8adc9aa3e5880b72997389144d0c402d89
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934004"
---
# <span data-ttu-id="ac600-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="ac600-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="ac600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac600-102">SYNOPSIS</span></span>
<span data-ttu-id="ac600-103">Eşitleme grubu eşitlemesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="ac600-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="ac600-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac600-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac600-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac600-105">DESCRIPTION</span></span>
<span data-ttu-id="ac600-106">**Stop-AzSqlSyncGroupSync** cmdlet 'i, eşitleme grubu eşitlemesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="ac600-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="ac600-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac600-107">EXAMPLES</span></span>

### <span data-ttu-id="ac600-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ac600-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="ac600-109">Bu komut, eşitleme grubu Kapsamım için devam eden eşitlemeyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="ac600-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="ac600-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac600-110">PARAMETERS</span></span>

### <span data-ttu-id="ac600-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ac600-111">-DatabaseName</span></span>
<span data-ttu-id="ac600-112">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="ac600-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ac600-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac600-113">-DefaultProfile</span></span>
<span data-ttu-id="ac600-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ac600-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac600-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ac600-115">-PassThru</span></span>
<span data-ttu-id="ac600-116">Eşitleme grubunun iade edilip edilmeyeceğini tanımlar</span><span class="sxs-lookup"><span data-stu-id="ac600-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="ac600-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac600-117">-ResourceGroupName</span></span>
<span data-ttu-id="ac600-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ac600-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="ac600-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ac600-119">-ServerName</span></span>
<span data-ttu-id="ac600-120">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="ac600-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ac600-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ac600-121">-SyncGroupName</span></span>
<span data-ttu-id="ac600-122">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ac600-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac600-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="ac600-123">-Confirm</span></span>
<span data-ttu-id="ac600-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ac600-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac600-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac600-125">-WhatIf</span></span>
<span data-ttu-id="ac600-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac600-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac600-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ac600-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac600-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac600-128">CommonParameters</span></span>
<span data-ttu-id="ac600-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac600-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac600-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ac600-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac600-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac600-131">INPUTS</span></span>

### <span data-ttu-id="ac600-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ac600-132">System.String</span></span>

## <span data-ttu-id="ac600-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac600-133">OUTPUTS</span></span>

### <span data-ttu-id="ac600-134">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="ac600-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="ac600-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac600-135">NOTES</span></span>

## <span data-ttu-id="ac600-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac600-136">RELATED LINKS</span></span>

[<span data-ttu-id="ac600-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="ac600-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

