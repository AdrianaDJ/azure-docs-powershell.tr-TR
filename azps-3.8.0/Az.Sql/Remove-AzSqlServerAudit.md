---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: ce9bf1a2c7b72e6da92c17e343a993294f8e335d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097800"
---
# <span data-ttu-id="6339e-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6339e-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="6339e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6339e-102">SYNOPSIS</span></span>
<span data-ttu-id="6339e-103">Azure SQL Server 'ın denetim ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6339e-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="6339e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6339e-104">SYNTAX</span></span>

### <span data-ttu-id="6339e-105">Sunucuparametrekümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6339e-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6339e-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6339e-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6339e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6339e-107">DESCRIPTION</span></span>
<span data-ttu-id="6339e-108">**Remove-AzSqlServerAudit** cmdlet 'i, BIR Azure SQL Server 'ın denetleme ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6339e-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="6339e-109">Sunucuyu tanımlayan *Resourcegroupname* ve *ServerName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6339e-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="6339e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6339e-110">EXAMPLES</span></span>

### <span data-ttu-id="6339e-111">Örnek 1: Azure SQL Server 'ın denetim ayarlarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6339e-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="6339e-112">Örnek 2: Azure SQL Server 'ın denetim ayarlarını ardışık düzen aracılığıyla kaldırma</span><span class="sxs-lookup"><span data-stu-id="6339e-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="6339e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6339e-113">PARAMETERS</span></span>

### <span data-ttu-id="6339e-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="6339e-114">-AsJob</span></span>
<span data-ttu-id="6339e-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6339e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6339e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6339e-116">-DefaultProfile</span></span>
<span data-ttu-id="6339e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6339e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6339e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6339e-118">-ResourceGroupName</span></span>
<span data-ttu-id="6339e-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6339e-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6339e-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6339e-120">-ServerName</span></span>
<span data-ttu-id="6339e-121">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="6339e-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6339e-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="6339e-122">-ServerObject</span></span>
<span data-ttu-id="6339e-123">Denetim ilkesini yönetmek için sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6339e-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6339e-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="6339e-124">-Confirm</span></span>
<span data-ttu-id="6339e-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6339e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6339e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6339e-126">-WhatIf</span></span>
<span data-ttu-id="6339e-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6339e-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6339e-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6339e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6339e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6339e-129">CommonParameters</span></span>
<span data-ttu-id="6339e-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6339e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6339e-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6339e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6339e-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6339e-132">INPUTS</span></span>

### <span data-ttu-id="6339e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6339e-133">System.String</span></span>

### <span data-ttu-id="6339e-134">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="6339e-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="6339e-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6339e-135">OUTPUTS</span></span>

### <span data-ttu-id="6339e-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6339e-136">System.Boolean</span></span>

## <span data-ttu-id="6339e-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6339e-137">NOTES</span></span>

## <span data-ttu-id="6339e-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6339e-138">RELATED LINKS</span></span>