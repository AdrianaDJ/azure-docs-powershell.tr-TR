---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/remove-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: c39a6cd64f48a7d8d6657499357daa1dd70fc091
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936008"
---
# <span data-ttu-id="5ce4e-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="5ce4e-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="5ce4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ce4e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce4e-103">Belirli bir galeri öğesini silme.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="5ce4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ce4e-104">SYNTAX</span></span>

### <span data-ttu-id="5ce4e-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5ce4e-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem -Name <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5ce4e-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="5ce4e-106">DeleteViaIdentity</span></span>
```
Remove-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5ce4e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ce4e-107">DESCRIPTION</span></span>
<span data-ttu-id="5ce4e-108">Belirli bir galeri öğesini silme.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="5ce4e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ce4e-109">EXAMPLES</span></span>

### <span data-ttu-id="5ce4e-110">Örnek 1: Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="5ce4e-110">Example 1: Remove-AzsGalleryItem</span></span>
```powershell
PS C:\> Remove-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

```

<span data-ttu-id="5ce4e-111">Azure yığın galerisinden TestUbuntu. test. 1.0.0 siler.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-111">Deletes TestUbuntu.Test.1.0.0 from Azure Stack gallery.</span></span>

### <span data-ttu-id="5ce4e-112">Örnek 2: ardışık düzen ile Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="5ce4e-112">Example 2: Remove-AzsGalleryItem through pipeline</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0 | Remove-AzsGalleryItem

```

<span data-ttu-id="5ce4e-113">TestUbuntu. test. 1.0.0 ile ardışık düzeni siler.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-113">Deletes TestUbuntu.Test.1.0.0 through pipeline.</span></span>

## <span data-ttu-id="5ce4e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ce4e-114">PARAMETERS</span></span>

### <span data-ttu-id="5ce4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce4e-115">-DefaultProfile</span></span>
<span data-ttu-id="5ce4e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5ce4e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ce4e-117">-InputObject</span></span>
<span data-ttu-id="5ce4e-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5ce4e-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5ce4e-119">-Name</span></span>
<span data-ttu-id="5ce4e-120">Galeri öğesinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-120">Identity of the gallery item.</span></span>
<span data-ttu-id="5ce4e-121">Publisher adını, öğe adını içerir ve süre karakteriyle ayrı sürüm içerebilir.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-121">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5ce4e-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5ce4e-122">-PassThru</span></span>
<span data-ttu-id="5ce4e-123">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="5ce4e-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5ce4e-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5ce4e-124">-SubscriptionId</span></span>
<span data-ttu-id="5ce4e-125">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5ce4e-126">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5ce4e-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="5ce4e-127">-Confirm</span></span>
<span data-ttu-id="5ce4e-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ce4e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce4e-129">-WhatIf</span></span>
<span data-ttu-id="5ce4e-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ce4e-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ce4e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce4e-132">CommonParameters</span></span>
<span data-ttu-id="5ce4e-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce4e-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce4e-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ce4e-135">INPUTS</span></span>

### <span data-ttu-id="5ce4e-136">Microsoft. Azure. PowerShell. cmdlet. Gallery. modeller. ıgalleryıdentity</span><span class="sxs-lookup"><span data-stu-id="5ce4e-136">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="5ce4e-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ce4e-137">OUTPUTS</span></span>

### <span data-ttu-id="5ce4e-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ce4e-138">System.Boolean</span></span>



## <span data-ttu-id="5ce4e-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ce4e-139">NOTES</span></span>

<span data-ttu-id="5ce4e-140">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ce4e-141">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5ce4e-142">INPUTOBJECT <IGalleryIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="5ce4e-142">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ce4e-143">`[GalleryItemName <String>]`: Galeri öğesinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-143">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="5ce4e-144">Publisher adını, öğe adını içerir ve süre karakteriyle ayrı sürüm içerebilir.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-144">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="5ce4e-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="5ce4e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ce4e-146">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5ce4e-147">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5ce4e-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5ce4e-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ce4e-148">RELATED LINKS</span></span>

