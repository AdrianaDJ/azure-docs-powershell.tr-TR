---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 915CBA29-5A58-4A5D-9F02-976CB76D4800
online version: ''
schema: 2.0.0
ms.openlocfilehash: af98cbdc0be73c87682d0ed004d17cd9e82c9baa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106175"
---
# <span data-ttu-id="fb4ff-101">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="fb4ff-101">Remove-AzureAclConfig</span></span>

## <span data-ttu-id="fb4ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4ff-103">Bir Azure sanal makine yapılandırmasından ACL yapılandırma nesnesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb4ff-103">Removes an ACL configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="fb4ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb4ff-104">SYNTAX</span></span>

```
Remove-AzureAclConfig [-EndpointName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fb4ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb4ff-105">DESCRIPTION</span></span>
<span data-ttu-id="fb4ff-106">**Remove-AzureAclConfig** cmdlet 'i Azure sanal makine yapılandırmasından bir erişim denetim LISTESI (ACL) yapılandırma nesnesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb4ff-106">The **Remove-AzureAclConfig** cmdlet removes an access control list (ACL) configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="fb4ff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb4ff-107">EXAMPLES</span></span>

### <span data-ttu-id="fb4ff-108">Örnek 1: ACL yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="fb4ff-108">Example 1: Remove an ACL configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureAclConfig -EndpointName "Web" | Update-AzureVM
```

<span data-ttu-id="fb4ff-109">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice adındaki hizmette VirtualMachine07 adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="fb4ff-109">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="fb4ff-110">Komut, ardışık düzen işlecini kullanarak nesneyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="fb4ff-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fb4ff-111">Bu cmdlet Web adlı uç noktanın ACL yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb4ff-111">That cmdlet removes the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="fb4ff-112">Komut, sonucu sanal makineyi güncelleştiren **-AzureVM** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="fb4ff-112">The command passes the result to the **Update-AzureVM** cmdlet, which updates the virtual machine.</span></span>

## <span data-ttu-id="fb4ff-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb4ff-113">PARAMETERS</span></span>

### <span data-ttu-id="fb4ff-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fb4ff-114">-EndpointName</span></span>
<span data-ttu-id="fb4ff-115">Bu cmdlet 'in ACL yapılandırmasını kaldırdığı uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb4ff-115">Specifies the name of the endpoint from which this cmdlet removes the ACL configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4ff-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fb4ff-116">-InformationAction</span></span>
<span data-ttu-id="fb4ff-117">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb4ff-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fb4ff-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fb4ff-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fb4ff-119">'A</span><span class="sxs-lookup"><span data-stu-id="fb4ff-119">Continue</span></span>
- <span data-ttu-id="fb4ff-120">Manıza</span><span class="sxs-lookup"><span data-stu-id="fb4ff-120">Ignore</span></span>
- <span data-ttu-id="fb4ff-121">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="fb4ff-121">Inquire</span></span>
- <span data-ttu-id="fb4ff-122">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="fb4ff-122">SilentlyContinue</span></span>
- <span data-ttu-id="fb4ff-123">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="fb4ff-123">Stop</span></span>
- <span data-ttu-id="fb4ff-124">Biliriz</span><span class="sxs-lookup"><span data-stu-id="fb4ff-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4ff-125">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fb4ff-125">-InformationVariable</span></span>
<span data-ttu-id="fb4ff-126">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb4ff-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4ff-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="fb4ff-127">-Profile</span></span>
<span data-ttu-id="fb4ff-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb4ff-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fb4ff-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fb4ff-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4ff-130">-VM</span><span class="sxs-lookup"><span data-stu-id="fb4ff-130">-VM</span></span>
<span data-ttu-id="fb4ff-131">Bu cmdlet 'in bir ACL yapılandırmasını kaldırdığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb4ff-131">Specifies the virtual machine from which this cmdlet removes an ACL configuration.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4ff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4ff-132">CommonParameters</span></span>
<span data-ttu-id="fb4ff-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb4ff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4ff-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb4ff-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4ff-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb4ff-135">INPUTS</span></span>

## <span data-ttu-id="fb4ff-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb4ff-136">OUTPUTS</span></span>

## <span data-ttu-id="fb4ff-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb4ff-137">NOTES</span></span>

## <span data-ttu-id="fb4ff-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb4ff-138">RELATED LINKS</span></span>

[<span data-ttu-id="fb4ff-139">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="fb4ff-139">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="fb4ff-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fb4ff-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="fb4ff-141">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="fb4ff-141">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="fb4ff-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="fb4ff-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)

[<span data-ttu-id="fb4ff-143">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fb4ff-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


