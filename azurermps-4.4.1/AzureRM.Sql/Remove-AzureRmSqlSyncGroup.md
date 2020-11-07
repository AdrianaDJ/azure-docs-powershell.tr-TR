---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 99892ee748de030a045bd9d0a022051206236198
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765041"
---
# <span data-ttu-id="f0c4c-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f0c4c-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="f0c4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c4c-103">Azure SQL veritabanı eşitleme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f0c4c-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0c4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0c4c-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0c4c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0c4c-105">DESCRIPTION</span></span>
<span data-ttu-id="f0c4c-106">**Remove-AzureRmSqlSyncGroup** cmdlet 'ı BIR Azure SQL veritabanı eşitleme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f0c4c-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="f0c4c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0c4c-107">EXAMPLES</span></span>

### <span data-ttu-id="f0c4c-108">Örnek 1: eşitleme grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="f0c4c-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="f0c4c-109">Bu komut, syncGroup01 adlı Azure SQL veritabanı eşitleme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f0c4c-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="f0c4c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0c4c-110">PARAMETERS</span></span>

### <span data-ttu-id="f0c4c-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="f0c4c-111">-Confirm</span></span>
<span data-ttu-id="f0c4c-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f0c4c-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0c4c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f0c4c-113">-DatabaseName</span></span>
<span data-ttu-id="f0c4c-114">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="f0c4c-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f0c4c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f0c4c-115">-Force</span></span>
<span data-ttu-id="f0c4c-116">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="f0c4c-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f0c4c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0c4c-117">-Name</span></span>
<span data-ttu-id="f0c4c-118">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f0c4c-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c4c-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f0c4c-119">-PassThru</span></span>
<span data-ttu-id="f0c4c-120">Kaldırılan eşitleme grubunu iade edilip edilmeyeceğini tanımlar</span><span class="sxs-lookup"><span data-stu-id="f0c4c-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="f0c4c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0c4c-121">-ResourceGroupName</span></span>
<span data-ttu-id="f0c4c-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f0c4c-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f0c4c-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f0c4c-123">-ServerName</span></span>
<span data-ttu-id="f0c4c-124">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="f0c4c-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f0c4c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0c4c-125">-WhatIf</span></span>
<span data-ttu-id="f0c4c-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0c4c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0c4c-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f0c4c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0c4c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c4c-128">-DefaultProfile</span></span>
<span data-ttu-id="f0c4c-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0c4c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0c4c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c4c-130">CommonParameters</span></span>
<span data-ttu-id="f0c4c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0c4c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c4c-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0c4c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c4c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0c4c-133">INPUTS</span></span>

## <span data-ttu-id="f0c4c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0c4c-134">OUTPUTS</span></span>

### <span data-ttu-id="f0c4c-135">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncgroupmodel</span><span class="sxs-lookup"><span data-stu-id="f0c4c-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="f0c4c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0c4c-136">NOTES</span></span>

## <span data-ttu-id="f0c4c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0c4c-137">RELATED LINKS</span></span>

[<span data-ttu-id="f0c4c-138">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f0c4c-138">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="f0c4c-139">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f0c4c-139">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="f0c4c-140">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f0c4c-140">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

