---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: e81667523327c9a83497ce4f586f166fe69d0dc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593783"
---
# <span data-ttu-id="c758d-101">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="c758d-101">Start-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="c758d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c758d-102">SYNOPSIS</span></span>
<span data-ttu-id="c758d-103">Eşitleme grubu eşitlemesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="c758d-103">Starts a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c758d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c758d-104">SYNTAX</span></span>

```
Start-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c758d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c758d-105">DESCRIPTION</span></span>
<span data-ttu-id="c758d-106">**Start-AzureRmSqlSyncGroupSync** cmdlet 'i, eşitleme grubu eşitlemesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="c758d-106">The **Start-AzureRmSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="c758d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c758d-107">EXAMPLES</span></span>

### <span data-ttu-id="c758d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c758d-108">Example 1</span></span>
```
PS C:\> Start-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="c758d-109">Bu komut, eşitleme grubu Kapsamım için eşitlemenin hepsini başlatır.</span><span class="sxs-lookup"><span data-stu-id="c758d-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="c758d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c758d-110">PARAMETERS</span></span>

### <span data-ttu-id="c758d-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="c758d-111">-Confirm</span></span>
<span data-ttu-id="c758d-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c758d-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c758d-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c758d-113">-DatabaseName</span></span>
<span data-ttu-id="c758d-114">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="c758d-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="c758d-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c758d-115">-PassThru</span></span>
<span data-ttu-id="c758d-116">Eşitleme grubunun iade edilip edilmeyeceğini tanımlar</span><span class="sxs-lookup"><span data-stu-id="c758d-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="c758d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c758d-117">-ResourceGroupName</span></span>
<span data-ttu-id="c758d-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c758d-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c758d-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c758d-119">-ServerName</span></span>
<span data-ttu-id="c758d-120">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="c758d-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="c758d-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c758d-121">-SyncGroupName</span></span>
<span data-ttu-id="c758d-122">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c758d-122">The sync group name.</span></span>

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

### <span data-ttu-id="c758d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c758d-123">-WhatIf</span></span>
<span data-ttu-id="c758d-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c758d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c758d-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c758d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c758d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c758d-126">-DefaultProfile</span></span>
<span data-ttu-id="c758d-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c758d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c758d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c758d-128">CommonParameters</span></span>
<span data-ttu-id="c758d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c758d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c758d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c758d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c758d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c758d-131">INPUTS</span></span>

## <span data-ttu-id="c758d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c758d-132">OUTPUTS</span></span>

### <span data-ttu-id="c758d-133">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="c758d-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="c758d-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c758d-134">NOTES</span></span>

## <span data-ttu-id="c758d-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c758d-135">RELATED LINKS</span></span>

[<span data-ttu-id="c758d-136">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="c758d-136">Stop-AzureRmSqlSyncGroupSync</span></span>](./Stop-AzureRmSqlSyncGroupSync.md)

