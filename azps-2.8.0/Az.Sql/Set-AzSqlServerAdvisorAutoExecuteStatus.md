---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: aa3aff9a1e471445c49cbfb23b5799a97c54025d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933754"
---
# <span data-ttu-id="db039-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="db039-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="db039-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db039-102">SYNOPSIS</span></span>
<span data-ttu-id="db039-103">Azure SQL Server Danışmanı 'nın otomatik yürütme durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="db039-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="db039-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db039-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db039-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db039-105">DESCRIPTION</span></span>
<span data-ttu-id="db039-106">**Set-Azsqlserverdanışmanlar Orautoexecutestatus** cmdlet 'ı, Azure SQL Server Danışmanı için otomatik yürütme özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="db039-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="db039-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db039-107">EXAMPLES</span></span>

### <span data-ttu-id="db039-108">Örnek 1: bir danışman için otomatik çalıştırmayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="db039-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="db039-109">Bu komut CreateIndex adındaki bir Advisor 'ın otomatik yürütme durumunu verir.</span><span class="sxs-lookup"><span data-stu-id="db039-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="db039-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db039-110">PARAMETERS</span></span>

### <span data-ttu-id="db039-111">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="db039-111">-AdvisorName</span></span>
<span data-ttu-id="db039-112">Bu cmdlet 'in otomatik yürütme durumunu güncelleştirdiği bir danışman adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db039-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db039-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="db039-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="db039-114">Bu cmdlet 'in otomatik yürütme durumunu güncelleştirdiği değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="db039-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="db039-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="db039-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db039-116">Etkin</span><span class="sxs-lookup"><span data-stu-id="db039-116">Enabled</span></span>
- <span data-ttu-id="db039-117">DISABLED</span><span class="sxs-lookup"><span data-stu-id="db039-117">Disabled</span></span>
- <span data-ttu-id="db039-118">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="db039-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db039-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db039-119">-DefaultProfile</span></span>
<span data-ttu-id="db039-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="db039-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db039-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db039-121">-ResourceGroupName</span></span>
<span data-ttu-id="db039-122">Sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db039-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="db039-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="db039-123">-ServerName</span></span>
<span data-ttu-id="db039-124">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db039-124">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db039-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="db039-125">-Confirm</span></span>
<span data-ttu-id="db039-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="db039-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db039-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db039-127">-WhatIf</span></span>
<span data-ttu-id="db039-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db039-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db039-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="db039-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db039-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db039-130">CommonParameters</span></span>
<span data-ttu-id="db039-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db039-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db039-132">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="db039-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db039-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db039-133">INPUTS</span></span>

### <span data-ttu-id="db039-134">System. String</span><span class="sxs-lookup"><span data-stu-id="db039-134">System.String</span></span>

### <span data-ttu-id="db039-135">Microsoft. Azure. Commands. Sql. Advisor. cmdlet. danışmanlar Orautoexecutestatus</span><span class="sxs-lookup"><span data-stu-id="db039-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="db039-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db039-136">OUTPUTS</span></span>

### <span data-ttu-id="db039-137">Microsoft. Azure. Commands. Sql. Advisor. model. Azuressqlserverdanışmanlar Ormodel</span><span class="sxs-lookup"><span data-stu-id="db039-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="db039-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db039-138">NOTES</span></span>
* <span data-ttu-id="db039-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, Server, MSSQL, danışman</span><span class="sxs-lookup"><span data-stu-id="db039-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="db039-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db039-140">RELATED LINKS</span></span>

[<span data-ttu-id="db039-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="db039-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="db039-142">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="db039-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
