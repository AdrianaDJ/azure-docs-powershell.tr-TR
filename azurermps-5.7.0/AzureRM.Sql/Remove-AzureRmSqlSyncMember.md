---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: b96d125b2a4f608c54024619ca6259a136d2ed69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588718"
---
# <span data-ttu-id="bdb6a-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bdb6a-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="bdb6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdb6a-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb6a-103">Azure SQL veritabanı eşitleme üyesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdb6a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bdb6a-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdb6a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bdb6a-105">DESCRIPTION</span></span>
<span data-ttu-id="bdb6a-106">**Remove-AzureRmSqlSyncMember** cmdlet 'ı BIR Azure SQL veritabanı eşitleme üyesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="bdb6a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bdb6a-107">EXAMPLES</span></span>

### <span data-ttu-id="bdb6a-108">Örnek 1: eşitleme üyesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="bdb6a-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="bdb6a-109">Bu komut, syncMember01 adındaki Azure SQL veritabanı eşitleme üyesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="bdb6a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bdb6a-110">PARAMETERS</span></span>

### <span data-ttu-id="bdb6a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bdb6a-111">-DatabaseName</span></span>
<span data-ttu-id="bdb6a-112">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb6a-113">-DefaultProfile</span></span>
<span data-ttu-id="bdb6a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bdb6a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb6a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bdb6a-115">-Force</span></span>
<span data-ttu-id="bdb6a-116">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="bdb6a-116">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb6a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="bdb6a-117">-Name</span></span>
<span data-ttu-id="bdb6a-118">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-118">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb6a-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bdb6a-119">-PassThru</span></span>
<span data-ttu-id="bdb6a-120">Kaldırılan eşitleme üyesini verip vermediğini tanımlar</span><span class="sxs-lookup"><span data-stu-id="bdb6a-120">Defines Whether return the removed sync member</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb6a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb6a-121">-ResourceGroupName</span></span>
<span data-ttu-id="bdb6a-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb6a-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bdb6a-123">-ServerName</span></span>
<span data-ttu-id="bdb6a-124">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-124">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb6a-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb6a-125">-SyncGroupName</span></span>
<span data-ttu-id="bdb6a-126">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb6a-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="bdb6a-127">-Confirm</span></span>
<span data-ttu-id="bdb6a-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb6a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdb6a-129">-WhatIf</span></span>
<span data-ttu-id="bdb6a-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdb6a-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb6a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb6a-132">CommonParameters</span></span>
<span data-ttu-id="bdb6a-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb6a-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdb6a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb6a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bdb6a-135">INPUTS</span></span>

### <span data-ttu-id="bdb6a-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bdb6a-136">None</span></span>
<span data-ttu-id="bdb6a-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="bdb6a-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bdb6a-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bdb6a-138">OUTPUTS</span></span>

### <span data-ttu-id="bdb6a-139">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncmembermodel</span><span class="sxs-lookup"><span data-stu-id="bdb6a-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="bdb6a-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bdb6a-140">NOTES</span></span>

## <span data-ttu-id="bdb6a-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bdb6a-141">RELATED LINKS</span></span>

[<span data-ttu-id="bdb6a-142">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bdb6a-142">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="bdb6a-143">Güncelleştirme-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bdb6a-143">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="bdb6a-144">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="bdb6a-144">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

