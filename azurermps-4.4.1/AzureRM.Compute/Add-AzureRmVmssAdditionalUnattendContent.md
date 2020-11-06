---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: d99e54439b2e8b4474c4b0123634ddd7c286ea9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586995"
---
# <span data-ttu-id="89e71-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="89e71-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="89e71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89e71-102">SYNOPSIS</span></span>
<span data-ttu-id="89e71-103">Katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="89e71-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89e71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89e71-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89e71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="89e71-105">DESCRIPTION</span></span>
<span data-ttu-id="89e71-106">**Add-AzureRmVmssAdditionalUnattendContent** cmdlet 'ı katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="89e71-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="89e71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89e71-107">EXAMPLES</span></span>

### <span data-ttu-id="89e71-108">Örnek 1: Katılımsız Windows kurulumu yanıt dosyasına bilgi ekleme</span><span class="sxs-lookup"><span data-stu-id="89e71-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="89e71-109">Bu komut katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="89e71-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="89e71-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89e71-110">PARAMETERS</span></span>

### <span data-ttu-id="89e71-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="89e71-111">-ComponentName</span></span>
<span data-ttu-id="89e71-112">Ekli içerikle yapılandırılacak bileşenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89e71-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="89e71-113">İzin verilen tek değer Microsoft-Windows-Shell-Setup ' dır.</span><span class="sxs-lookup"><span data-stu-id="89e71-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="89e71-114">-İçerik</span><span class="sxs-lookup"><span data-stu-id="89e71-114">-Content</span></span>
<span data-ttu-id="89e71-115">Belirtilen yol ve bileşen için unattend.xml dosyasına eklenen XML biçimli içeriği belirtir.</span><span class="sxs-lookup"><span data-stu-id="89e71-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="89e71-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e71-116">-DefaultProfile</span></span>
<span data-ttu-id="89e71-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89e71-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89e71-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="89e71-118">-PassName</span></span>
<span data-ttu-id="89e71-119">İçeriğin uygulandığı geçiş adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89e71-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="89e71-120">İzin verilen tek değer oobeSystem değeridir.</span><span class="sxs-lookup"><span data-stu-id="89e71-120">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="89e71-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="89e71-121">-SettingName</span></span>
<span data-ttu-id="89e71-122">İçeriğin uygulandığı ayarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89e71-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="89e71-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="89e71-123">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="89e71-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="89e71-124">FirstLogonCommands</span></span>
- <span data-ttu-id="89e71-125">Açmayı</span><span class="sxs-lookup"><span data-stu-id="89e71-125">AutoLogon</span></span>

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

### <span data-ttu-id="89e71-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="89e71-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="89e71-127">Sanal makine **ölçeği kümesi** nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="89e71-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="89e71-128">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="89e71-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="89e71-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="89e71-129">-Confirm</span></span>
<span data-ttu-id="89e71-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89e71-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89e71-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89e71-131">-WhatIf</span></span>
<span data-ttu-id="89e71-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89e71-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89e71-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89e71-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89e71-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e71-134">CommonParameters</span></span>
<span data-ttu-id="89e71-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89e71-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e71-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89e71-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e71-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89e71-137">INPUTS</span></span>

## <span data-ttu-id="89e71-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89e71-138">OUTPUTS</span></span>

## <span data-ttu-id="89e71-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89e71-139">NOTES</span></span>

## <span data-ttu-id="89e71-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89e71-140">RELATED LINKS</span></span>

[<span data-ttu-id="89e71-141">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="89e71-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
