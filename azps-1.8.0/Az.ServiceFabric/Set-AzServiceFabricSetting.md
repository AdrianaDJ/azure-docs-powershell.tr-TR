---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: cea8ec21021725bae99ef597a33079621f539cec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759103"
---
# <span data-ttu-id="bfc91-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="bfc91-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="bfc91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfc91-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc91-103">Kümeye bir veya birden çok hizmet yapısı ayarı ekleyin veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="bfc91-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="bfc91-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bfc91-104">SYNTAX</span></span>

### <span data-ttu-id="bfc91-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="bfc91-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc91-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="bfc91-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfc91-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bfc91-107">DESCRIPTION</span></span>
<span data-ttu-id="bfc91-108">Kümedeki hizmet doku ayarlarını eklemek veya güncelleştirmek için **set-AzServiceFabricSetting** kullanın.</span><span class="sxs-lookup"><span data-stu-id="bfc91-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="bfc91-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bfc91-109">EXAMPLES</span></span>

### <span data-ttu-id="bfc91-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bfc91-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="bfc91-111">Bu komut, ' NamingService ' bölümünün altındaki ' MaxFileOperationTimeout ' değerini ' 5000 ' olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bfc91-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="bfc91-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bfc91-112">PARAMETERS</span></span>

### <span data-ttu-id="bfc91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc91-113">-DefaultProfile</span></span>
<span data-ttu-id="bfc91-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bfc91-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfc91-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="bfc91-115">-Name</span></span>
<span data-ttu-id="bfc91-116">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="bfc91-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc91-117">-Parametre</span><span class="sxs-lookup"><span data-stu-id="bfc91-117">-Parameter</span></span>
<span data-ttu-id="bfc91-118">Parametresi.</span><span class="sxs-lookup"><span data-stu-id="bfc91-118">Parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc91-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc91-119">-ResourceGroupName</span></span>
<span data-ttu-id="bfc91-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfc91-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bfc91-121">-Bölüm</span><span class="sxs-lookup"><span data-stu-id="bfc91-121">-Section</span></span>
<span data-ttu-id="bfc91-122">Bölümde.</span><span class="sxs-lookup"><span data-stu-id="bfc91-122">Section.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc91-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="bfc91-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="bfc91-124">İstemci kimlik doğrulama türü.</span><span class="sxs-lookup"><span data-stu-id="bfc91-124">Client authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc91-125">-Değer</span><span class="sxs-lookup"><span data-stu-id="bfc91-125">-Value</span></span>
<span data-ttu-id="bfc91-126">Değerlerini.</span><span class="sxs-lookup"><span data-stu-id="bfc91-126">Value.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc91-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="bfc91-127">-Confirm</span></span>
<span data-ttu-id="bfc91-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bfc91-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfc91-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfc91-129">-WhatIf</span></span>
<span data-ttu-id="bfc91-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bfc91-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfc91-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bfc91-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfc91-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc91-132">CommonParameters</span></span>
<span data-ttu-id="bfc91-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bfc91-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc91-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfc91-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc91-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bfc91-135">INPUTS</span></span>

### <span data-ttu-id="bfc91-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bfc91-136">System.String</span></span>

### <span data-ttu-id="bfc91-137">Microsoft. Azure. Commands. ServiceFabric. modeller. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="bfc91-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="bfc91-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bfc91-138">OUTPUTS</span></span>

### <span data-ttu-id="bfc91-139">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="bfc91-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="bfc91-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bfc91-140">NOTES</span></span>

## <span data-ttu-id="bfc91-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bfc91-141">RELATED LINKS</span></span>
