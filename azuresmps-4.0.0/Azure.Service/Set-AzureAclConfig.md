---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106432"
---
# <span data-ttu-id="60318-101">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="60318-101">Set-AzureAclConfig</span></span>

## <span data-ttu-id="60318-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60318-102">SYNOPSIS</span></span>
<span data-ttu-id="60318-103">ACL yapılandırma nesnesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="60318-103">Modifies an ACL configuration object.</span></span>

## <span data-ttu-id="60318-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60318-104">SYNTAX</span></span>

### <span data-ttu-id="60318-105">AddRule</span><span class="sxs-lookup"><span data-stu-id="60318-105">AddRule</span></span>
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="60318-106">RemoveRule</span><span class="sxs-lookup"><span data-stu-id="60318-106">RemoveRule</span></span>
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="60318-107">SetRule</span><span class="sxs-lookup"><span data-stu-id="60318-107">SetRule</span></span>
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="60318-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="60318-108">DESCRIPTION</span></span>
<span data-ttu-id="60318-109">**Set-AzureAclConfig** cmdlet 'i, var olan Azure sanal makine yapılandırmasından bir erişim denetim LISTESI (ACL) yapılandırma nesnesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="60318-109">The **Set-AzureAclConfig** cmdlet modifies an access control list (ACL) configuration object from an existing Azure virtual machine configuration.</span></span>

## <span data-ttu-id="60318-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60318-110">EXAMPLES</span></span>

### <span data-ttu-id="60318-111">Örnek 1: yeni bir ACL yapılandırmasına kural ekleme</span><span class="sxs-lookup"><span data-stu-id="60318-111">Example 1: Add a rule to a new ACL configuration</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

<span data-ttu-id="60318-112">İlk komut bir ACL yapılandırması oluşturur ve $Acl değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="60318-112">The first command creates an ACL configuration, and then stores it in the $Acl variable.</span></span>

<span data-ttu-id="60318-113">İkinci komut, $Acl depolanan yapılandırmaya yeni bir kural ekler.</span><span class="sxs-lookup"><span data-stu-id="60318-113">The second command adds a new rule to the configuration stored in $Acl.</span></span>
<span data-ttu-id="60318-114">Komut, kuralın bir eylemini, alt ağını, sıralamasını ve açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60318-114">The command specifies an action, subnet, order, and description for the rule.</span></span>

### <span data-ttu-id="60318-115">Örnek 2: ACL yapılandırmasındaki bir kuralı değiştirme</span><span class="sxs-lookup"><span data-stu-id="60318-115">Example 2: Modify a rule in an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="60318-116">İlk komut, VirtualMachine07 adındaki sanal makineyi, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice adındaki hizmette alır.</span><span class="sxs-lookup"><span data-stu-id="60318-116">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="60318-117">Komut, bu nesneyi ardışık düzen işlecini kullanarak **Get-AzureAclConfig** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="60318-117">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="60318-118">Bu cmdlet Web adlı uç noktanın ACL yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="60318-118">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="60318-119">Komut bu ACL yapılandırma nesnesini $Acl değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="60318-119">The command stores that ACL configuration object in the $Acl variable.</span></span>

<span data-ttu-id="60318-120">İkinci komut, KIMLIĞI 0 olan kuralı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="60318-120">The second command modifies the rule that has the ID of 0.</span></span>
<span data-ttu-id="60318-121">Komut, kuralın sırasını ve açıklamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="60318-121">The command changes the order and the description of the rule.</span></span>

<span data-ttu-id="60318-122">Son komutu, **set-AzureEndpoint** cmdlet 'ini kullanarak bu sanal makinenin ACL yapılandırma nesnesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="60318-122">The final command sets the ACL configuration object for that virtual machine by using the **Set-AzureEndpoint** cmdlet.</span></span>
<span data-ttu-id="60318-123">Bu komut, bu sanal makineyi de güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="60318-123">The command also updates that virtual machine.</span></span>

### <span data-ttu-id="60318-124">Örnek 3: ACL yapılandırmasından kural kaldırma</span><span class="sxs-lookup"><span data-stu-id="60318-124">Example 3: Remove a rule from an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="60318-125">İlk komut $Acl değişkeninde bir ACL yapılandırma nesnesini depolar.</span><span class="sxs-lookup"><span data-stu-id="60318-125">The first command stores an ACL configuration object in the $Acl variable.</span></span>
<span data-ttu-id="60318-126">Bu, önceki örnekle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="60318-126">This is the same as the previous example.</span></span>

<span data-ttu-id="60318-127">İkinci komut, KIMLIĞI 0 olan kuralı $Acl ACL yapılandırmasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="60318-127">The second command removes the rule that has the ID 0 from the ACL configuration in $Acl.</span></span>

<span data-ttu-id="60318-128">Son komutu sanal makinenin ACL yapılandırma nesnesini ayarlar ve bu sanal makineyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="60318-128">The final command sets the ACL configuration object for the virtual machine and updates that virtual machine.</span></span>
<span data-ttu-id="60318-129">Bu, önceki örnekle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="60318-129">This is the same as the previous example.</span></span>

## <span data-ttu-id="60318-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60318-130">PARAMETERS</span></span>

### <span data-ttu-id="60318-131">-ACL</span><span class="sxs-lookup"><span data-stu-id="60318-131">-ACL</span></span>
<span data-ttu-id="60318-132">Bu cmdlet 'in değiştirdiği bir ACL yapılandırma nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="60318-132">Specifies an ACL configuration object that this cmdlet modifies.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60318-133">-Eylem</span><span class="sxs-lookup"><span data-stu-id="60318-133">-Action</span></span>
<span data-ttu-id="60318-134">Bu cmdlet 'in eklediği veya değiştirdiği kuralın eylemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="60318-134">Specifies the action for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="60318-135">Geçerli değerler: Izin ver ve Reddet.</span><span class="sxs-lookup"><span data-stu-id="60318-135">Valid values are: Permit and Deny.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60318-136">-AddRule</span><span class="sxs-lookup"><span data-stu-id="60318-136">-AddRule</span></span>
<span data-ttu-id="60318-137">Bu cmdlet 'in ACL yapılandırmasına kural eklediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="60318-137">Indicates that this cmdlet adds a rule to the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60318-138">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="60318-138">-Description</span></span>
<span data-ttu-id="60318-139">Bu cmdlet 'in eklediği veya değiştirdiği kuralın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60318-139">Specifies a description for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60318-140">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="60318-140">-InformationAction</span></span>
<span data-ttu-id="60318-141">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="60318-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="60318-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="60318-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="60318-143">'A</span><span class="sxs-lookup"><span data-stu-id="60318-143">Continue</span></span>
- <span data-ttu-id="60318-144">Manıza</span><span class="sxs-lookup"><span data-stu-id="60318-144">Ignore</span></span>
- <span data-ttu-id="60318-145">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="60318-145">Inquire</span></span>
- <span data-ttu-id="60318-146">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="60318-146">SilentlyContinue</span></span>
- <span data-ttu-id="60318-147">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="60318-147">Stop</span></span>
- <span data-ttu-id="60318-148">Biliriz</span><span class="sxs-lookup"><span data-stu-id="60318-148">Suspend</span></span>

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

### <span data-ttu-id="60318-149">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="60318-149">-InformationVariable</span></span>
<span data-ttu-id="60318-150">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="60318-150">Specifies an information variable.</span></span>

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

### <span data-ttu-id="60318-151">-Düzen</span><span class="sxs-lookup"><span data-stu-id="60318-151">-Order</span></span>
<span data-ttu-id="60318-152">Bu cmdlet 'in eklediği veya değiştirdiği kuralın işlem sırasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60318-152">Specifies the processing order for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60318-153">-RemoteSubnet</span><span class="sxs-lookup"><span data-stu-id="60318-153">-RemoteSubnet</span></span>
<span data-ttu-id="60318-154">Bu cmdlet 'in eklediği veya değiştirdiği kuralın uzaktaki alt ağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60318-154">Specifies the remote subnet for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="60318-155">Sınıfsız Etki alanları arası yönlendirme (CıDR) biçimindeki bir adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="60318-155">Specifies an address in Classless Interdomain Routing (CIDR) format.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60318-156">-RemoveRule</span><span class="sxs-lookup"><span data-stu-id="60318-156">-RemoveRule</span></span>
<span data-ttu-id="60318-157">Bu cmdlet 'in ACL yapılandırmasından kural kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="60318-157">Indicates that this cmdlet removes a rule from the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60318-158">-RuleId</span><span class="sxs-lookup"><span data-stu-id="60318-158">-RuleId</span></span>
<span data-ttu-id="60318-159">Bu cmdlet 'in kaldırdığı veya ACL yapılandırması için değiştirdiği kuralın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="60318-159">Specifies the ID of the rule that this cmdlet removes or modifies for the ACL configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60318-160">-SetRule</span><span class="sxs-lookup"><span data-stu-id="60318-160">-SetRule</span></span>
<span data-ttu-id="60318-161">Bu cmdlet 'in ACL yapılandırmasındaki bir kuralı değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="60318-161">Indicates that this cmdlet modifies a rule in the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60318-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60318-162">CommonParameters</span></span>
<span data-ttu-id="60318-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60318-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60318-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60318-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60318-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60318-165">INPUTS</span></span>

## <span data-ttu-id="60318-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60318-166">OUTPUTS</span></span>

## <span data-ttu-id="60318-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60318-167">NOTES</span></span>

## <span data-ttu-id="60318-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60318-168">RELATED LINKS</span></span>

[<span data-ttu-id="60318-169">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="60318-169">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="60318-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="60318-170">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="60318-171">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="60318-171">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="60318-172">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="60318-172">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="60318-173">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="60318-173">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="60318-174">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="60318-174">Update-AzureVM</span></span>](./Update-AzureVM.md)


