---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: d09f0032d44a0558c1052f1dcfc3a3c94a7dff00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278283"
---
# <span data-ttu-id="89caf-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="89caf-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="89caf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89caf-102">SYNOPSIS</span></span>
<span data-ttu-id="89caf-103">Eşitleme grubu eşitlemesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="89caf-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="89caf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89caf-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89caf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="89caf-105">DESCRIPTION</span></span>
<span data-ttu-id="89caf-106">**Stop-AzSqlSyncGroupSync** cmdlet 'i, eşitleme grubu eşitlemesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="89caf-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="89caf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89caf-107">EXAMPLES</span></span>

### <span data-ttu-id="89caf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="89caf-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="89caf-109">Bu komut, eşitleme grubu Kapsamım için devam eden eşitlemeyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="89caf-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="89caf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89caf-110">PARAMETERS</span></span>

### <span data-ttu-id="89caf-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="89caf-111">-DatabaseName</span></span>
<span data-ttu-id="89caf-112">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="89caf-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="89caf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89caf-113">-DefaultProfile</span></span>
<span data-ttu-id="89caf-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="89caf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89caf-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="89caf-115">-PassThru</span></span>
<span data-ttu-id="89caf-116">Eşitleme grubunun iade edilip edilmeyeceğini tanımlar</span><span class="sxs-lookup"><span data-stu-id="89caf-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="89caf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89caf-117">-ResourceGroupName</span></span>
<span data-ttu-id="89caf-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="89caf-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="89caf-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="89caf-119">-ServerName</span></span>
<span data-ttu-id="89caf-120">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="89caf-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="89caf-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="89caf-121">-SyncGroupName</span></span>
<span data-ttu-id="89caf-122">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="89caf-122">The sync group name.</span></span>

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

### <span data-ttu-id="89caf-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="89caf-123">-Confirm</span></span>
<span data-ttu-id="89caf-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89caf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89caf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89caf-125">-WhatIf</span></span>
<span data-ttu-id="89caf-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89caf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89caf-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89caf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89caf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89caf-128">CommonParameters</span></span>
<span data-ttu-id="89caf-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89caf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89caf-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="89caf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89caf-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89caf-131">INPUTS</span></span>

### <span data-ttu-id="89caf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="89caf-132">System.String</span></span>

## <span data-ttu-id="89caf-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89caf-133">OUTPUTS</span></span>

### <span data-ttu-id="89caf-134">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="89caf-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="89caf-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89caf-135">NOTES</span></span>

## <span data-ttu-id="89caf-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89caf-136">RELATED LINKS</span></span>

[<span data-ttu-id="89caf-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="89caf-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

