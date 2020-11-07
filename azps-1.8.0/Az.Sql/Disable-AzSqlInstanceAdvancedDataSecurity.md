---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 872189e5219b1e4d7079664d190450ed2dd4bebb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759060"
---
# <span data-ttu-id="024a7-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="024a7-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="024a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="024a7-102">SYNOPSIS</span></span>
<span data-ttu-id="024a7-103">Yönetilen örnekte gelişmiş veri güvenliğini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="024a7-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="024a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="024a7-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="024a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="024a7-105">DESCRIPTION</span></span>
<span data-ttu-id="024a7-106">**Disable-Azsqlınstanceadvancevseçdatasecurity** cmdlet 'i yönetilen örnekte gelişmiş veri güvenliğini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="024a7-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="024a7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="024a7-107">EXAMPLES</span></span>

### <span data-ttu-id="024a7-108">Örnek 1-yönetilen örneği gelişmiş veri güvenliğini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="024a7-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="024a7-109">Örnek 2-yönetilen örnek kaynağından sunucu gelişmiş veri güvenliğini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="024a7-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="024a7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="024a7-110">PARAMETERS</span></span>

### <span data-ttu-id="024a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="024a7-111">-DefaultProfile</span></span>
<span data-ttu-id="024a7-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="024a7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="024a7-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="024a7-113">-InputObject</span></span>
<span data-ttu-id="024a7-114">Gelişmiş veri güvenliği ilkesi işlemiyle kullanılacak yönetilen örnek nesnesi</span><span class="sxs-lookup"><span data-stu-id="024a7-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="024a7-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="024a7-115">-InstanceName</span></span>
<span data-ttu-id="024a7-116">SQL veritabanı yönetilen örnek adı.</span><span class="sxs-lookup"><span data-stu-id="024a7-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="024a7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="024a7-117">-ResourceGroupName</span></span>
<span data-ttu-id="024a7-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="024a7-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="024a7-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="024a7-119">-Confirm</span></span>
<span data-ttu-id="024a7-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="024a7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="024a7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="024a7-121">-WhatIf</span></span>
<span data-ttu-id="024a7-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="024a7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="024a7-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="024a7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="024a7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="024a7-124">CommonParameters</span></span>
<span data-ttu-id="024a7-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="024a7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="024a7-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="024a7-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="024a7-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="024a7-127">INPUTS</span></span>

### <span data-ttu-id="024a7-128">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="024a7-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="024a7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="024a7-129">System.String</span></span>

## <span data-ttu-id="024a7-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="024a7-130">OUTPUTS</span></span>

### <span data-ttu-id="024a7-131">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. Managedınstanceadvanceddatasecuritypolicymodel</span><span class="sxs-lookup"><span data-stu-id="024a7-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="024a7-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="024a7-132">NOTES</span></span>

## <span data-ttu-id="024a7-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="024a7-133">RELATED LINKS</span></span>
