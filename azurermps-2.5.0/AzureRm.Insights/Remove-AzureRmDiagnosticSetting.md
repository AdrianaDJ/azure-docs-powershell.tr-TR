---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermdiagnosticsetting
schema: 2.0.0
ms.openlocfilehash: 2555b7e5523ff739976bb30021250d684ffc6af1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940130"
---
# <span data-ttu-id="0548b-101">Remove-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="0548b-101">Remove-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="0548b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0548b-102">SYNOPSIS</span></span>
<span data-ttu-id="0548b-103">Kaynağın tanı ayarını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="0548b-103">Remove a diagnostic setting for the a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0548b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0548b-104">SYNTAX</span></span>

```
Remove-AzureRmDiagnosticSetting -ResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0548b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0548b-105">DESCRIPTION</span></span>
<span data-ttu-id="0548b-106">**Remove-AzureRmDiagnosticSetting** cmdlet 'i, belirli bir kaynağın tanılama ayarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0548b-106">The **Remove-AzureRmDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="0548b-107">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="0548b-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="0548b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0548b-108">EXAMPLES</span></span>

### <span data-ttu-id="0548b-109">Örnek 1: kaynağın varsayılan tanılama ayarını (hizmet) kaldırma</span><span class="sxs-lookup"><span data-stu-id="0548b-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzureRmDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="0548b-110">Bu komut, Resource01 adındaki kaynağın varsayılan tanılama ayarını (hizmet) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0548b-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="0548b-111">Örnek 2: kaynak için verilen adla tanımlanan varsayılan tanılama ayarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0548b-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzureRmDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="0548b-112">Bu komut, Resource01 adlı kaynak için myDiagSetting adlı tanı ayarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0548b-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="0548b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0548b-113">PARAMETERS</span></span>

### <span data-ttu-id="0548b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0548b-114">-DefaultProfile</span></span>
<span data-ttu-id="0548b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0548b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0548b-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0548b-116">-Name</span></span>
<span data-ttu-id="0548b-117">Tanılama ayarının adı.</span><span class="sxs-lookup"><span data-stu-id="0548b-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="0548b-118">Verilmezse, önceki API 'da olduğu gibi "servis" için çağrı yapın ve bu cmdlet yalnızca ölçümler/Günlükler için tüm kategorileri devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="0548b-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="0548b-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0548b-119">-ResourceId</span></span>
<span data-ttu-id="0548b-120">Kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0548b-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="0548b-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="0548b-121">-Confirm</span></span>
<span data-ttu-id="0548b-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0548b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0548b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0548b-123">-WhatIf</span></span>
<span data-ttu-id="0548b-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0548b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0548b-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0548b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0548b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0548b-126">CommonParameters</span></span>
<span data-ttu-id="0548b-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0548b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0548b-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0548b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0548b-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0548b-129">INPUTS</span></span>

### <span data-ttu-id="0548b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0548b-130">System.String</span></span>

## <span data-ttu-id="0548b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0548b-131">OUTPUTS</span></span>

### <span data-ttu-id="0548b-132">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0548b-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0548b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0548b-133">NOTES</span></span>

## <span data-ttu-id="0548b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0548b-134">RELATED LINKS</span></span>

<span data-ttu-id="0548b-135">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md) 
 [Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="0548b-135">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)
[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)</span></span>
