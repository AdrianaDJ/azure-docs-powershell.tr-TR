---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273975"
---
# <span data-ttu-id="d4286-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d4286-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="d4286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4286-102">SYNOPSIS</span></span>
<span data-ttu-id="d4286-103">IoT güvenlik çözümünü silme</span><span class="sxs-lookup"><span data-stu-id="d4286-103">Delete IoT security solution</span></span>

## <span data-ttu-id="d4286-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4286-104">SYNTAX</span></span>

### <span data-ttu-id="d4286-105">ResourceGroupLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d4286-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4286-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="d4286-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4286-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d4286-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4286-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4286-108">DESCRIPTION</span></span>
<span data-ttu-id="d4286-109">Remove-AzIotSecuritySolution cmdlet 'i belirli bir IoT güvenlik çözümünü siler.</span><span class="sxs-lookup"><span data-stu-id="d4286-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="d4286-110">IoT güvenlik çözümü, tehditlere karşı korunmaya ve saptamasını engellemeye yardımcı olmak için IoT aygıtlarından ve IoT Hub 'dan güvenlik verilerini ve olayları toplar.</span><span class="sxs-lookup"><span data-stu-id="d4286-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="d4286-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4286-111">EXAMPLES</span></span>

### <span data-ttu-id="d4286-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d4286-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d4286-113">"MyResourceGroup" kaynak grubuyla "Myörnek" IoT güvenlik çözümünü silme</span><span class="sxs-lookup"><span data-stu-id="d4286-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="d4286-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4286-114">PARAMETERS</span></span>

### <span data-ttu-id="d4286-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4286-115">-DefaultProfile</span></span>
<span data-ttu-id="d4286-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4286-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4286-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4286-117">-InputObject</span></span>
<span data-ttu-id="d4286-118">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d4286-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4286-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4286-119">-Name</span></span>
<span data-ttu-id="d4286-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="d4286-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4286-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d4286-121">-PassThru</span></span>
<span data-ttu-id="d4286-122">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="d4286-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="d4286-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4286-123">-ResourceGroupName</span></span>
<span data-ttu-id="d4286-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d4286-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4286-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d4286-125">-ResourceId</span></span>
<span data-ttu-id="d4286-126">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d4286-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4286-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="d4286-127">-Confirm</span></span>
<span data-ttu-id="d4286-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d4286-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4286-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4286-129">-WhatIf</span></span>
<span data-ttu-id="d4286-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d4286-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4286-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d4286-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4286-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4286-132">CommonParameters</span></span>
<span data-ttu-id="d4286-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4286-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4286-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d4286-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4286-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4286-135">INPUTS</span></span>

### <span data-ttu-id="d4286-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d4286-136">System.String</span></span>

### <span data-ttu-id="d4286-137">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d4286-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="d4286-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4286-138">OUTPUTS</span></span>

### <span data-ttu-id="d4286-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4286-139">System.Boolean</span></span>

## <span data-ttu-id="d4286-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4286-140">NOTES</span></span>

## <span data-ttu-id="d4286-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4286-141">RELATED LINKS</span></span>
