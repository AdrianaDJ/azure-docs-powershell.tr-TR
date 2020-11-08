---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 791658e9f4f10fdbb8b1000d6b1bc88d392aaf46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273858"
---
# <span data-ttu-id="41b96-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="41b96-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="41b96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41b96-102">SYNOPSIS</span></span>
<span data-ttu-id="41b96-103">Azure SQL Server DNS diğer adının işaret olduğu sunucuyu değiştirir</span><span class="sxs-lookup"><span data-stu-id="41b96-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="41b96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41b96-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41b96-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="41b96-105">DESCRIPTION</span></span>
<span data-ttu-id="41b96-106">Bu komut, sunucunun diğer adına işaret etmekte olduğunu güncelleştiriyor.</span><span class="sxs-lookup"><span data-stu-id="41b96-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="41b96-107">Bu komutun, diğer adın gittiği yeni sunucunun bulunduğu abonede oturumu açıkken verilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="41b96-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="41b96-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41b96-108">EXAMPLES</span></span>

### <span data-ttu-id="41b96-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="41b96-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="41b96-110">Bu komut, daha önce eski sunucu 'ya</span><span class="sxs-lookup"><span data-stu-id="41b96-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="41b96-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41b96-111">PARAMETERS</span></span>

### <span data-ttu-id="41b96-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="41b96-112">-AsJob</span></span>
<span data-ttu-id="41b96-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="41b96-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41b96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b96-114">-DefaultProfile</span></span>
<span data-ttu-id="41b96-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="41b96-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41b96-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="41b96-116">-Name</span></span>
<span data-ttu-id="41b96-117">Azure SQL Server DNS diğer adı.</span><span class="sxs-lookup"><span data-stu-id="41b96-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b96-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41b96-118">-ResourceGroupName</span></span>
<span data-ttu-id="41b96-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="41b96-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b96-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="41b96-120">-SourceServerName</span></span>
<span data-ttu-id="41b96-121">Diğer adın işaret etmekte olduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="41b96-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b96-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41b96-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="41b96-123">Kaynak sunucunun kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="41b96-123">The name of resource group of the source server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b96-124">-Sourceserversubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="41b96-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="41b96-125">Kaynak sunucunun abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="41b96-125">The subscription id of the source server</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b96-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="41b96-126">-TargetServerName</span></span>
<span data-ttu-id="41b96-127">Diğer adın işaret edeceği Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="41b96-127">The name of Azure Sql Server to which alias should point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b96-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="41b96-128">-Confirm</span></span>
<span data-ttu-id="41b96-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="41b96-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41b96-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41b96-130">-WhatIf</span></span>
<span data-ttu-id="41b96-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="41b96-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41b96-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="41b96-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41b96-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b96-133">CommonParameters</span></span>
<span data-ttu-id="41b96-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41b96-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b96-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="41b96-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b96-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41b96-136">INPUTS</span></span>

### <span data-ttu-id="41b96-137">System. String</span><span class="sxs-lookup"><span data-stu-id="41b96-137">System.String</span></span>

## <span data-ttu-id="41b96-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41b96-138">OUTPUTS</span></span>

### <span data-ttu-id="41b96-139">Microsoft. Azure. Commands. Sql. Serverdnsalıas. model. Azuressqlserverdnsaliasmodel</span><span class="sxs-lookup"><span data-stu-id="41b96-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="41b96-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41b96-140">NOTES</span></span>

## <span data-ttu-id="41b96-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41b96-141">RELATED LINKS</span></span>
