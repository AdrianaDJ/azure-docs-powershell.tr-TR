---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
ms.openlocfilehash: b357c44afd52dd398631b9b7edfcedb0360cf377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762344"
---
# <span data-ttu-id="7e259-101">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7e259-101">Remove-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="7e259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e259-102">SYNOPSIS</span></span>
<span data-ttu-id="7e259-103">Azure SQL eşitleme aracısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e259-103">Removes an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e259-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e259-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e259-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e259-105">DESCRIPTION</span></span>
<span data-ttu-id="7e259-106">**Remove-AzureRmSqlSyncAgent** cmdlet 'ı BIR Azure SQL eşitleme aracısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e259-106">The **Remove-AzureRmSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="7e259-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e259-107">EXAMPLES</span></span>

### <span data-ttu-id="7e259-108">Örnek 1: eşitleme aracısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7e259-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="7e259-109">Bu komut, syncAgent01 adındaki Azure SQL eşitleme aracısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e259-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="7e259-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e259-110">PARAMETERS</span></span>

### <span data-ttu-id="7e259-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e259-111">-DefaultProfile</span></span>
<span data-ttu-id="7e259-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7e259-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e259-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7e259-113">-Force</span></span>
<span data-ttu-id="7e259-114">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="7e259-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7e259-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e259-115">-Name</span></span>
<span data-ttu-id="7e259-116">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="7e259-116">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e259-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7e259-117">-PassThru</span></span>
<span data-ttu-id="7e259-118">Kaldırılan eşitleme aracısının döndürülmesini Isteyip Istemediğinizi tanımlar</span><span class="sxs-lookup"><span data-stu-id="7e259-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="7e259-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e259-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e259-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7e259-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e259-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7e259-121">-ServerName</span></span>
<span data-ttu-id="7e259-122">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="7e259-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="7e259-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e259-123">-Confirm</span></span>
<span data-ttu-id="7e259-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e259-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e259-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e259-125">-WhatIf</span></span>
<span data-ttu-id="7e259-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e259-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e259-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e259-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e259-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e259-128">CommonParameters</span></span>
<span data-ttu-id="7e259-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e259-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e259-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e259-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e259-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e259-131">INPUTS</span></span>

### <span data-ttu-id="7e259-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7e259-132">None</span></span>
<span data-ttu-id="7e259-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7e259-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e259-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e259-134">OUTPUTS</span></span>

### <span data-ttu-id="7e259-135">Microsoft. Azure. Commands. Sql. DataSync. model. azureskalite syncagentı</span><span class="sxs-lookup"><span data-stu-id="7e259-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="7e259-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e259-136">NOTES</span></span>

## <span data-ttu-id="7e259-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e259-137">RELATED LINKS</span></span>

[<span data-ttu-id="7e259-138">Yeni-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7e259-138">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="7e259-139">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7e259-139">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

