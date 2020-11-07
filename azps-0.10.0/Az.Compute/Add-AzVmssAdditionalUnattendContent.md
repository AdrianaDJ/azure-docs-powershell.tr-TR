---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 38f510602259ca799c6df947b9d74984dff178ba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937089"
---
# <span data-ttu-id="64623-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="64623-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="64623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64623-102">SYNOPSIS</span></span>
<span data-ttu-id="64623-103">Katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="64623-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="64623-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64623-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64623-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64623-105">DESCRIPTION</span></span>
<span data-ttu-id="64623-106">**Add-AzVmssAdditionalUnattendContent** cmdlet 'ı katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="64623-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="64623-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64623-107">EXAMPLES</span></span>

### <span data-ttu-id="64623-108">Örnek 1: Katılımsız Windows kurulumu yanıt dosyasına bilgi ekleme</span><span class="sxs-lookup"><span data-stu-id="64623-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="64623-109">Bu komut katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="64623-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="64623-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64623-110">PARAMETERS</span></span>

### <span data-ttu-id="64623-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="64623-111">-ComponentName</span></span>
<span data-ttu-id="64623-112">Ekli içerikle yapılandırılacak bileşenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64623-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="64623-113">İzin verilen tek değer Microsoft-Windows-Shell-Setup ' dır.</span><span class="sxs-lookup"><span data-stu-id="64623-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: ComponentNames
Parameter Sets: (All)
Aliases: 
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64623-114">-İçerik</span><span class="sxs-lookup"><span data-stu-id="64623-114">-Content</span></span>
<span data-ttu-id="64623-115">Belirtilen yol ve bileşen için unattend.xml dosyasına eklenen XML biçimli içeriği belirtir.</span><span class="sxs-lookup"><span data-stu-id="64623-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64623-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64623-116">-DefaultProfile</span></span>
<span data-ttu-id="64623-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64623-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64623-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="64623-118">-PassName</span></span>
<span data-ttu-id="64623-119">İçeriğin uygulandığı geçiş adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64623-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="64623-120">İzin verilen tek değer oobeSystem değeridir.</span><span class="sxs-lookup"><span data-stu-id="64623-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: PassNames
Parameter Sets: (All)
Aliases: 
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64623-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="64623-121">-SettingName</span></span>
<span data-ttu-id="64623-122">İçeriğin uygulandığı ayarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64623-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="64623-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="64623-123">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="64623-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="64623-124">FirstLogonCommands</span></span>
- <span data-ttu-id="64623-125">Açmayı</span><span class="sxs-lookup"><span data-stu-id="64623-125">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64623-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="64623-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="64623-127">Sanal makine **ölçeği kümesi** nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="64623-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="64623-128">Nesneyi oluşturmak için [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64623-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64623-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="64623-129">-Confirm</span></span>
<span data-ttu-id="64623-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="64623-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64623-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64623-131">-WhatIf</span></span>
<span data-ttu-id="64623-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="64623-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64623-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="64623-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64623-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64623-134">CommonParameters</span></span>
<span data-ttu-id="64623-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64623-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64623-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64623-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64623-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64623-137">INPUTS</span></span>

### <span data-ttu-id="64623-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="64623-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="64623-139">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="64623-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="64623-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64623-140">OUTPUTS</span></span>

### <span data-ttu-id="64623-141">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="64623-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="64623-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64623-142">NOTES</span></span>

## <span data-ttu-id="64623-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64623-143">RELATED LINKS</span></span>

[<span data-ttu-id="64623-144">Yeni-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="64623-144">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
