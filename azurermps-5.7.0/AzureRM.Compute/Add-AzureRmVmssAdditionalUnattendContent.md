---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: de61efcbabb2e5acd7d82bf7a1cec8341fe06433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588985"
---
# <span data-ttu-id="d2d7f-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="d2d7f-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="d2d7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2d7f-102">SYNOPSIS</span></span>
<span data-ttu-id="d2d7f-103">Katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2d7f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2d7f-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2d7f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2d7f-105">DESCRIPTION</span></span>
<span data-ttu-id="d2d7f-106">**Add-AzureRmVmssAdditionalUnattendContent** cmdlet 'ı katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="d2d7f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2d7f-107">EXAMPLES</span></span>

### <span data-ttu-id="d2d7f-108">Örnek 1: Katılımsız Windows kurulumu yanıt dosyasına bilgi ekleme</span><span class="sxs-lookup"><span data-stu-id="d2d7f-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="d2d7f-109">Bu komut katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="d2d7f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2d7f-110">PARAMETERS</span></span>

### <span data-ttu-id="d2d7f-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="d2d7f-111">-ComponentName</span></span>
<span data-ttu-id="d2d7f-112">Ekli içerikle yapılandırılacak bileşenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="d2d7f-113">İzin verilen tek değer Microsoft-Windows-Shell-Setup ' dır.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="d2d7f-114">-İçerik</span><span class="sxs-lookup"><span data-stu-id="d2d7f-114">-Content</span></span>
<span data-ttu-id="d2d7f-115">Belirtilen yol ve bileşen için unattend.xml dosyasına eklenen XML biçimli içeriği belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="d2d7f-116">-PassName</span><span class="sxs-lookup"><span data-stu-id="d2d7f-116">-PassName</span></span>
<span data-ttu-id="d2d7f-117">İçeriğin uygulandığı geçiş adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-117">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="d2d7f-118">İzin verilen tek değer oobeSystem değeridir.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-118">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="d2d7f-119">-SettingName</span><span class="sxs-lookup"><span data-stu-id="d2d7f-119">-SettingName</span></span>
<span data-ttu-id="d2d7f-120">İçeriğin uygulandığı ayarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-120">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="d2d7f-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d2d7f-121">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="d2d7f-122">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="d2d7f-122">FirstLogonCommands</span></span>
- <span data-ttu-id="d2d7f-123">Açmayı</span><span class="sxs-lookup"><span data-stu-id="d2d7f-123">AutoLogon</span></span>

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

### <span data-ttu-id="d2d7f-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d2d7f-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d2d7f-125">Sanal makine **ölçeği kümesi** nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-125">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="d2d7f-126">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2d7f-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2d7f-127">-Confirm</span></span>
<span data-ttu-id="d2d7f-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2d7f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2d7f-129">-WhatIf</span></span>
<span data-ttu-id="d2d7f-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2d7f-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2d7f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d7f-132">CommonParameters</span></span>
<span data-ttu-id="d2d7f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d7f-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2d7f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d7f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2d7f-135">INPUTS</span></span>

### <span data-ttu-id="d2d7f-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d2d7f-136">None</span></span>
<span data-ttu-id="d2d7f-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d2d7f-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2d7f-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2d7f-138">OUTPUTS</span></span>

## <span data-ttu-id="d2d7f-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2d7f-139">NOTES</span></span>

## <span data-ttu-id="d2d7f-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2d7f-140">RELATED LINKS</span></span>

[<span data-ttu-id="d2d7f-141">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d2d7f-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
