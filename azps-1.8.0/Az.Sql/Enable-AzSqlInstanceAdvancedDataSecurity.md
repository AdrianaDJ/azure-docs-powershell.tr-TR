---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: faf93387f068c6ee8e83653d31b96a1f3ecdef70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759058"
---
# <span data-ttu-id="98f17-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="98f17-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="98f17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98f17-102">SYNOPSIS</span></span>
<span data-ttu-id="98f17-103">Yönetilen örnekte gelişmiş veri güvenliğini verir.</span><span class="sxs-lookup"><span data-stu-id="98f17-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="98f17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98f17-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98f17-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98f17-105">DESCRIPTION</span></span>
<span data-ttu-id="98f17-106">**Enable-Azsqlınstanceadvancevseçdatasecurity** cmdlet 'i yönetilen örnekte gelişmiş veri güvenliğini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="98f17-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="98f17-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98f17-107">EXAMPLES</span></span>

### <span data-ttu-id="98f17-108">Örnek 1-yönetilen örneği gelişmiş veri güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="98f17-108">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="98f17-109">Örnek 2-sunucu kaynağından yönetilen örnek gelişmiş veri güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="98f17-109">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="98f17-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98f17-110">PARAMETERS</span></span>

### <span data-ttu-id="98f17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f17-111">-DefaultProfile</span></span>
<span data-ttu-id="98f17-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98f17-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98f17-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98f17-113">-InputObject</span></span>
<span data-ttu-id="98f17-114">Gelişmiş veri güvenliği ilkesi işlemiyle kullanılacak yönetilen örnek nesnesi</span><span class="sxs-lookup"><span data-stu-id="98f17-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="98f17-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="98f17-115">-InstanceName</span></span>
<span data-ttu-id="98f17-116">SQL veritabanı yönetilen örnek adı.</span><span class="sxs-lookup"><span data-stu-id="98f17-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="98f17-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f17-117">-ResourceGroupName</span></span>
<span data-ttu-id="98f17-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="98f17-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="98f17-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="98f17-119">-Confirm</span></span>
<span data-ttu-id="98f17-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="98f17-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98f17-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98f17-121">-WhatIf</span></span>
<span data-ttu-id="98f17-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="98f17-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98f17-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="98f17-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98f17-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f17-124">CommonParameters</span></span>
<span data-ttu-id="98f17-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98f17-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f17-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="98f17-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f17-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98f17-127">INPUTS</span></span>

### <span data-ttu-id="98f17-128">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="98f17-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="98f17-129">System. String</span><span class="sxs-lookup"><span data-stu-id="98f17-129">System.String</span></span>

## <span data-ttu-id="98f17-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98f17-130">OUTPUTS</span></span>

### <span data-ttu-id="98f17-131">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. Managedınstanceadvanceddatasecuritypolicymodel</span><span class="sxs-lookup"><span data-stu-id="98f17-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="98f17-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98f17-132">NOTES</span></span>

## <span data-ttu-id="98f17-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98f17-133">RELATED LINKS</span></span>
