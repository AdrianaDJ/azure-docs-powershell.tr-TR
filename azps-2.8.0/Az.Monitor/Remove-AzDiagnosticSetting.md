---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: 26b736cbbbdde599c951a1e555ec159cfd9bb12d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932162"
---
# <span data-ttu-id="b4dd6-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="b4dd6-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="b4dd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="b4dd6-103">Kaynağın tanı ayarını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="b4dd6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4dd6-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4dd6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4dd6-105">DESCRIPTION</span></span>
<span data-ttu-id="b4dd6-106">**Remove-AzDiagnosticSetting** cmdlet 'i, belirli bir kaynağın tanılama ayarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="b4dd6-107">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b4dd6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4dd6-108">EXAMPLES</span></span>

### <span data-ttu-id="b4dd6-109">Örnek 1: kaynağın varsayılan tanılama ayarını (hizmet) kaldırma</span><span class="sxs-lookup"><span data-stu-id="b4dd6-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="b4dd6-110">Bu komut, Resource01 adındaki kaynağın varsayılan tanılama ayarını (hizmet) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="b4dd6-111">Örnek 2: kaynak için verilen adla tanımlanan varsayılan tanılama ayarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b4dd6-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="b4dd6-112">Bu komut, Resource01 adlı kaynak için myDiagSetting adlı tanı ayarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="b4dd6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4dd6-113">PARAMETERS</span></span>

### <span data-ttu-id="b4dd6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4dd6-114">-DefaultProfile</span></span>
<span data-ttu-id="b4dd6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4dd6-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4dd6-116">-Name</span></span>
<span data-ttu-id="b4dd6-117">Tanılama ayarının adı.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="b4dd6-118">Verilmezse, önceki API 'da olduğu gibi "servis" için çağrı yapın ve bu cmdlet yalnızca ölçümler/Günlükler için tüm kategorileri devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4dd6-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b4dd6-119">-ResourceId</span></span>
<span data-ttu-id="b4dd6-120">Kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="b4dd6-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4dd6-121">-Confirm</span></span>
<span data-ttu-id="b4dd6-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4dd6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4dd6-123">-WhatIf</span></span>
<span data-ttu-id="b4dd6-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4dd6-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4dd6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4dd6-126">CommonParameters</span></span>
<span data-ttu-id="b4dd6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4dd6-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b4dd6-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4dd6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4dd6-129">INPUTS</span></span>

### <span data-ttu-id="b4dd6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b4dd6-130">System.String</span></span>

## <span data-ttu-id="b4dd6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4dd6-131">OUTPUTS</span></span>

### <span data-ttu-id="b4dd6-132">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b4dd6-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b4dd6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4dd6-133">NOTES</span></span>

## <span data-ttu-id="b4dd6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4dd6-134">RELATED LINKS</span></span>

<span data-ttu-id="b4dd6-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="b4dd6-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
