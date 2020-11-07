---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 278c80206e1221550afc5c603c618c8219ea152f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933497"
---
# <span data-ttu-id="99b43-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="99b43-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="99b43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99b43-102">SYNOPSIS</span></span>
<span data-ttu-id="99b43-103">Yönetilen örnekte gelişmiş veri güvenliğini verir.</span><span class="sxs-lookup"><span data-stu-id="99b43-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="99b43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99b43-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99b43-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99b43-105">DESCRIPTION</span></span>
<span data-ttu-id="99b43-106">**Enable-Azsqlınstanceadvancevseçdatasecurity** cmdlet 'i yönetilen örnekte gelişmiş veri güvenliğini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="99b43-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="99b43-107">Gelişmiş veri güvenliği, yönetilen örneğiniz için veri sınıflandırması, güvenlik açığı değerlendirmesi ve Gelişmiş tehdit koruması içeren Birleşik bir güvenlik paketidir.</span><span class="sxs-lookup"><span data-stu-id="99b43-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="99b43-108">(Güvenlik açığı değerlendirmelerinin kaydedilmesi için yeni bir depolama hesabı otomatik olarak oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="99b43-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="99b43-109">Bu amaçla önceden bir depolama hesabı oluşturulduysa, bunun yerine bu bir hesap kullanılır.</span><span class="sxs-lookup"><span data-stu-id="99b43-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="99b43-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99b43-110">EXAMPLES</span></span>

### <span data-ttu-id="99b43-111">Örnek 1-yönetilen örneği gelişmiş veri güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="99b43-111">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="99b43-112">Örnek 2-sunucu kaynağından yönetilen örnek gelişmiş veri güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="99b43-112">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="99b43-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99b43-113">PARAMETERS</span></span>

### <span data-ttu-id="99b43-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="99b43-114">-AsJob</span></span>
<span data-ttu-id="99b43-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="99b43-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99b43-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b43-116">-DefaultProfile</span></span>
<span data-ttu-id="99b43-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99b43-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99b43-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="99b43-118">-DeploymentName</span></span>
<span data-ttu-id="99b43-119">Gelişmiş veri güvenliği dağıtımı için özel bir ad sağlayın</span><span class="sxs-lookup"><span data-stu-id="99b43-119">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="99b43-120">-Donotconfiguredüzeltme.</span><span class="sxs-lookup"><span data-stu-id="99b43-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="99b43-121">Güvenlik açığı değerlendirmesini otomatik olarak etkinleştirmeyin (Bu, depolama hesabı oluşturmaz)</span><span class="sxs-lookup"><span data-stu-id="99b43-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="99b43-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99b43-122">-InputObject</span></span>
<span data-ttu-id="99b43-123">Gelişmiş veri güvenliği ilkesi işlemiyle kullanılacak yönetilen örnek nesnesi</span><span class="sxs-lookup"><span data-stu-id="99b43-123">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99b43-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="99b43-124">-InstanceName</span></span>
<span data-ttu-id="99b43-125">SQL veritabanı yönetilen örnek adı.</span><span class="sxs-lookup"><span data-stu-id="99b43-125">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="99b43-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99b43-126">-ResourceGroupName</span></span>
<span data-ttu-id="99b43-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="99b43-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="99b43-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="99b43-128">-Confirm</span></span>
<span data-ttu-id="99b43-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="99b43-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99b43-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99b43-130">-WhatIf</span></span>
<span data-ttu-id="99b43-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99b43-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99b43-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="99b43-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99b43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b43-133">CommonParameters</span></span>
<span data-ttu-id="99b43-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99b43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b43-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99b43-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b43-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99b43-136">INPUTS</span></span>

### <span data-ttu-id="99b43-137">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="99b43-137">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="99b43-138">System. String</span><span class="sxs-lookup"><span data-stu-id="99b43-138">System.String</span></span>

## <span data-ttu-id="99b43-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99b43-139">OUTPUTS</span></span>

### <span data-ttu-id="99b43-140">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. Managedınstanceadvanceddatasecuritypolicymodel</span><span class="sxs-lookup"><span data-stu-id="99b43-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="99b43-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99b43-141">NOTES</span></span>

## <span data-ttu-id="99b43-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99b43-142">RELATED LINKS</span></span>
