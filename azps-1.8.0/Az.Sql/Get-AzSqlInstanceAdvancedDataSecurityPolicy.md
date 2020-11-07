---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 3f67d8197fd56cbcb615e8d95ef4331910ff9080
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758977"
---
# <span data-ttu-id="35bd2-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="35bd2-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="35bd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="35bd2-103">Yönetilen bir örneğin gelişmiş veri güvenliği ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="35bd2-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="35bd2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35bd2-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35bd2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="35bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="35bd2-106">Yönetilen bir örneğin gelişmiş veri güvenliği ilkesini gösteren **Get-Azsqlınstanceadvancevseçdatasecuritma** cmdlet 'i.</span><span class="sxs-lookup"><span data-stu-id="35bd2-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrives the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="35bd2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35bd2-107">EXAMPLES</span></span>

### <span data-ttu-id="35bd2-108">Örnek 1-yönetilen örnek gelişmiş veri güvenliğini alır</span><span class="sxs-lookup"><span data-stu-id="35bd2-108">Example 1 - Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="35bd2-109">Örnek 2-yönetilen örneğe gelişmiş veri güvenliğini yönetilen örnek kaynağından alır</span><span class="sxs-lookup"><span data-stu-id="35bd2-109">Example 2 - Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="35bd2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35bd2-110">PARAMETERS</span></span>

### <span data-ttu-id="35bd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35bd2-111">-DefaultProfile</span></span>
<span data-ttu-id="35bd2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="35bd2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35bd2-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35bd2-113">-InputObject</span></span>
<span data-ttu-id="35bd2-114">Gelişmiş veri güvenliği ilkesi işlemiyle kullanılacak yönetilen örnek nesnesi</span><span class="sxs-lookup"><span data-stu-id="35bd2-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="35bd2-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="35bd2-115">-InstanceName</span></span>
<span data-ttu-id="35bd2-116">SQL veritabanı yönetilen örnek adı.</span><span class="sxs-lookup"><span data-stu-id="35bd2-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="35bd2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35bd2-117">-ResourceGroupName</span></span>
<span data-ttu-id="35bd2-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="35bd2-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="35bd2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35bd2-119">CommonParameters</span></span>
<span data-ttu-id="35bd2-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35bd2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35bd2-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="35bd2-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35bd2-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35bd2-122">INPUTS</span></span>

### <span data-ttu-id="35bd2-123">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="35bd2-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="35bd2-124">System. String</span><span class="sxs-lookup"><span data-stu-id="35bd2-124">System.String</span></span>

## <span data-ttu-id="35bd2-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35bd2-125">OUTPUTS</span></span>

### <span data-ttu-id="35bd2-126">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. model. Managedınstanceadvanceddatasecuritypolicymodel</span><span class="sxs-lookup"><span data-stu-id="35bd2-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="35bd2-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35bd2-127">NOTES</span></span>

## <span data-ttu-id="35bd2-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35bd2-128">RELATED LINKS</span></span>
