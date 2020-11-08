---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268371"
---
# <span data-ttu-id="ccbbf-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="ccbbf-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="ccbbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccbbf-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbbf-103">Katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="ccbbf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ccbbf-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccbbf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ccbbf-105">DESCRIPTION</span></span>
<span data-ttu-id="ccbbf-106">**Add-AzVmssAdditionalUnattendContent** cmdlet 'ı katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="ccbbf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ccbbf-107">EXAMPLES</span></span>

### <span data-ttu-id="ccbbf-108">Örnek 1: Katılımsız Windows kurulumu yanıt dosyasına bilgi ekleme</span><span class="sxs-lookup"><span data-stu-id="ccbbf-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="ccbbf-109">Bu komut katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="ccbbf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ccbbf-110">PARAMETERS</span></span>

### <span data-ttu-id="ccbbf-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="ccbbf-111">-ComponentName</span></span>
<span data-ttu-id="ccbbf-112">Ekli içerikle yapılandırılacak bileşenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="ccbbf-113">İzin verilen tek değer Microsoft-Windows-Shell-Setup ' dır.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ComponentNames]
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbbf-114">-İçerik</span><span class="sxs-lookup"><span data-stu-id="ccbbf-114">-Content</span></span>
<span data-ttu-id="ccbbf-115">Belirtilen yol ve bileşen için unattend.xml dosyasına eklenen XML biçimli içeriği belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbbf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbbf-116">-DefaultProfile</span></span>
<span data-ttu-id="ccbbf-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccbbf-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="ccbbf-118">-PassName</span></span>
<span data-ttu-id="ccbbf-119">İçeriğin uygulandığı geçiş adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="ccbbf-120">İzin verilen tek değer oobeSystem değeridir.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.PassNames]
Parameter Sets: (All)
Aliases:
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbbf-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="ccbbf-121">-SettingName</span></span>
<span data-ttu-id="ccbbf-122">İçeriğin uygulandığı ayarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="ccbbf-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ccbbf-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="ccbbf-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="ccbbf-124">FirstLogonCommands</span></span>
- <span data-ttu-id="ccbbf-125">Açmayı</span><span class="sxs-lookup"><span data-stu-id="ccbbf-125">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbbf-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ccbbf-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ccbbf-127">Sanal makine **ölçeği kümesi** nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="ccbbf-128">Nesneyi oluşturmak için [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbbf-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="ccbbf-129">-Confirm</span></span>
<span data-ttu-id="ccbbf-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccbbf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccbbf-131">-WhatIf</span></span>
<span data-ttu-id="ccbbf-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccbbf-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccbbf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbbf-134">CommonParameters</span></span>
<span data-ttu-id="ccbbf-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbbf-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ccbbf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbbf-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ccbbf-137">INPUTS</span></span>

### <span data-ttu-id="ccbbf-138">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ccbbf-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ccbbf-139">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. PassNames, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ccbbf-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ccbbf-140">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. ComponentNames, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ccbbf-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ccbbf-141">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. SettingNames, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ccbbf-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ccbbf-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ccbbf-142">System.String</span></span>

## <span data-ttu-id="ccbbf-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ccbbf-143">OUTPUTS</span></span>

### <span data-ttu-id="ccbbf-144">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ccbbf-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ccbbf-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ccbbf-145">NOTES</span></span>

## <span data-ttu-id="ccbbf-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ccbbf-146">RELATED LINKS</span></span>

[<span data-ttu-id="ccbbf-147">Yeni-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ccbbf-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
