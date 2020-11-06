---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 9cd213aea4e6211f52b076fca753385aefb1b449
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589278"
---
# <span data-ttu-id="1e6c8-101">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="1e6c8-101">Stop-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="1e6c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e6c8-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6c8-103">Eşitleme grubu eşitlemesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="1e6c8-103">Stops a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e6c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e6c8-104">SYNTAX</span></span>

```
Stop-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e6c8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e6c8-105">DESCRIPTION</span></span>
<span data-ttu-id="1e6c8-106">**Stop-AzureRmSqlSyncGroupSync** cmdlet 'i, eşitleme grubu eşitlemesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="1e6c8-106">The **Stop-AzureRmSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="1e6c8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e6c8-107">EXAMPLES</span></span>

### <span data-ttu-id="1e6c8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1e6c8-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="1e6c8-109">Bu komut, eşitleme grubu Kapsamım için devam eden eşitlemeyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="1e6c8-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="1e6c8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e6c8-110">PARAMETERS</span></span>

### <span data-ttu-id="1e6c8-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1e6c8-111">-DatabaseName</span></span>
<span data-ttu-id="1e6c8-112">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="1e6c8-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1e6c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6c8-113">-DefaultProfile</span></span>
<span data-ttu-id="1e6c8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1e6c8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e6c8-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1e6c8-115">-PassThru</span></span>
<span data-ttu-id="1e6c8-116">Eşitleme grubunun iade edilip edilmeyeceğini tanımlar</span><span class="sxs-lookup"><span data-stu-id="1e6c8-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="1e6c8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6c8-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e6c8-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1e6c8-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="1e6c8-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1e6c8-119">-ServerName</span></span>
<span data-ttu-id="1e6c8-120">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="1e6c8-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="1e6c8-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6c8-121">-SyncGroupName</span></span>
<span data-ttu-id="1e6c8-122">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1e6c8-122">The sync group name.</span></span>

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

### <span data-ttu-id="1e6c8-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="1e6c8-123">-Confirm</span></span>
<span data-ttu-id="1e6c8-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1e6c8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e6c8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e6c8-125">-WhatIf</span></span>
<span data-ttu-id="1e6c8-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e6c8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e6c8-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1e6c8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e6c8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6c8-128">CommonParameters</span></span>
<span data-ttu-id="1e6c8-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e6c8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6c8-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e6c8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6c8-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e6c8-131">INPUTS</span></span>

### <span data-ttu-id="1e6c8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1e6c8-132">System.String</span></span>

## <span data-ttu-id="1e6c8-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e6c8-133">OUTPUTS</span></span>

### <span data-ttu-id="1e6c8-134">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="1e6c8-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="1e6c8-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e6c8-135">NOTES</span></span>

## <span data-ttu-id="1e6c8-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e6c8-136">RELATED LINKS</span></span>

[<span data-ttu-id="1e6c8-137">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="1e6c8-137">Start-AzureRmSqlSyncGroupSync</span></span>](./Start-AzureRmSqlSyncGroupSync.md)

