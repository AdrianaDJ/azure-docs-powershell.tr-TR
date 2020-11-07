---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: c2c3b634eb5a9e031c375a6cc696298becd58e8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933496"
---
# <span data-ttu-id="1ae6d-101">Enable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="1ae6d-101">Enable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="1ae6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ae6d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae6d-103">Sunucuda gelişmiş veri güvenliğini mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="1ae6d-103">Enables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="1ae6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ae6d-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ae6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ae6d-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae6d-106">**Enable-Azsqlserveradvancevseçdatasecurity** cmdlet 'ı sunucuda gelişmiş veri güvenliğini sağlar.</span><span class="sxs-lookup"><span data-stu-id="1ae6d-106">The **Enable-AzSqlServerAdvancedDataSecurity** cmdlet enables Advanced Data Security on a server.</span></span> <span data-ttu-id="1ae6d-107">Gelişmiş veri güvenliği, verileriniz için veri sınıflandırması, güvenlik açığı değerlendirmesi ve Gelişmiş tehdit koruması içeren Birleşik bir güvenlik paketidir.</span><span class="sxs-lookup"><span data-stu-id="1ae6d-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your server.</span></span> <span data-ttu-id="1ae6d-108">(Güvenlik açığı değerlendirmelerinin kaydedilmesi için yeni bir depolama hesabı otomatik olarak oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="1ae6d-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="1ae6d-109">Bu amaçla önceden bir depolama hesabı oluşturulduysa, bunun yerine bu bir hesap kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1ae6d-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="1ae6d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ae6d-110">EXAMPLES</span></span>

### <span data-ttu-id="1ae6d-111">Örnek 1-sunucu gelişmiş veri güvenliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="1ae6d-111">Example 1 - Enable server Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="1ae6d-112">Örnek 2-sunucu kaynağından gelişmiş veri güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="1ae6d-112">Example 2 - Enable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="1ae6d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ae6d-113">PARAMETERS</span></span>

### <span data-ttu-id="1ae6d-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="1ae6d-114">-AsJob</span></span>
<span data-ttu-id="1ae6d-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1ae6d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ae6d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae6d-116">-DefaultProfile</span></span>
<span data-ttu-id="1ae6d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ae6d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ae6d-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="1ae6d-118">-DeploymentName</span></span>
<span data-ttu-id="1ae6d-119">Gelişmiş veri güvenliği dağıtımı için özel bir ad sağlayın</span><span class="sxs-lookup"><span data-stu-id="1ae6d-119">Supply a custom name for Advanced Data Security deployment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae6d-120">-Donotconfiguredüzeltme.</span><span class="sxs-lookup"><span data-stu-id="1ae6d-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="1ae6d-121">Güvenlik açığı değerlendirmesini otomatik olarak etkinleştirmeyin (Bu, depolama hesabı oluşturmaz)</span><span class="sxs-lookup"><span data-stu-id="1ae6d-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="1ae6d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ae6d-122">-InputObject</span></span>
<span data-ttu-id="1ae6d-123">Gelişmiş veri güvenliği ilkesi işlemiyle kullanılacak sunucu nesnesi</span><span class="sxs-lookup"><span data-stu-id="1ae6d-123">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae6d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae6d-124">-ResourceGroupName</span></span>
<span data-ttu-id="1ae6d-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1ae6d-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ae6d-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1ae6d-126">-ServerName</span></span>
<span data-ttu-id="1ae6d-127">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="1ae6d-127">SQL Database server name.</span></span>

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

### <span data-ttu-id="1ae6d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="1ae6d-128">-Confirm</span></span>
<span data-ttu-id="1ae6d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1ae6d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae6d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae6d-130">-WhatIf</span></span>
<span data-ttu-id="1ae6d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ae6d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ae6d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1ae6d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae6d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae6d-133">CommonParameters</span></span>
<span data-ttu-id="1ae6d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ae6d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae6d-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae6d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae6d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ae6d-136">INPUTS</span></span>

### <span data-ttu-id="1ae6d-137">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="1ae6d-137">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="1ae6d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1ae6d-138">System.String</span></span>

## <span data-ttu-id="1ae6d-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ae6d-139">OUTPUTS</span></span>

### <span data-ttu-id="1ae6d-140">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="1ae6d-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="1ae6d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ae6d-141">NOTES</span></span>

## <span data-ttu-id="1ae6d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ae6d-142">RELATED LINKS</span></span>
