---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 89612136023173d2f725c8c4b286a270400f8c6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764193"
---
# <span data-ttu-id="3d748-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="3d748-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="3d748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d748-102">SYNOPSIS</span></span>
<span data-ttu-id="3d748-103">Bir API yönetim özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3d748-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d748-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d748-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d748-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d748-105">DESCRIPTION</span></span>
<span data-ttu-id="3d748-106">**Set-Azurermapsananagementproperty** cmdlet 'ı BIR Azure API yönetim özelliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3d748-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="3d748-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d748-107">EXAMPLES</span></span>

### <span data-ttu-id="3d748-108">Örnek 1: bir özellikte etiketleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="3d748-108">Example 1: Change the tags on a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="3d748-109">İlk komut $Tags değişkenine iki değer atar.</span><span class="sxs-lookup"><span data-stu-id="3d748-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="3d748-110">İkinci komut Property11 KIMLIĞINE sahip özelliği değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3d748-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="3d748-111">Komut, $Tags dizeleri özellik üzerinde etiket olarak atar.</span><span class="sxs-lookup"><span data-stu-id="3d748-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="3d748-112">Örnek 2: bir özelliği gizli değeri olacak şekilde değiştirme</span><span class="sxs-lookup"><span data-stu-id="3d748-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="3d748-113">Bu komut, özelliği şifrelenecek şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3d748-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="3d748-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d748-114">PARAMETERS</span></span>

### <span data-ttu-id="3d748-115">-Context</span><span class="sxs-lookup"><span data-stu-id="3d748-115">-Context</span></span>
<span data-ttu-id="3d748-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d748-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d748-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d748-117">-DefaultProfile</span></span>
<span data-ttu-id="3d748-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d748-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3d748-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d748-119">-Name</span></span>
<span data-ttu-id="3d748-120">Özelliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d748-120">Specifies the name of the property.</span></span>
<span data-ttu-id="3d748-121">Maksimum Uzunluk 100 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="3d748-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="3d748-122">Adlar yalnızca harf, rakam, nokta, çizgi ve alt çizgi karakterlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="3d748-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d748-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3d748-123">-PassThru</span></span>
<span data-ttu-id="3d748-124">Bu cmdlet 'in değiştirdiği **Psapsananagementözelliğini** geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d748-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d748-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="3d748-125">-PropertyId</span></span>
<span data-ttu-id="3d748-126">Bu cmdlet 'in değiştirdiği özelliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d748-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d748-127">-Parola</span><span class="sxs-lookup"><span data-stu-id="3d748-127">-Secret</span></span>
<span data-ttu-id="3d748-128">Özellik değerinin gizli olduğunu ve şifrelenmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d748-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d748-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3d748-129">-Tag</span></span>
<span data-ttu-id="3d748-130">Bir özellikle ilişkilendirilmiş Etiketler.</span><span class="sxs-lookup"><span data-stu-id="3d748-130">Tags associated with a property.</span></span> <span data-ttu-id="3d748-131">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="3d748-131">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d748-132">-Değer</span><span class="sxs-lookup"><span data-stu-id="3d748-132">-Value</span></span>
<span data-ttu-id="3d748-133">Özellik için bir değer belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d748-133">Specifies a value for the property.</span></span>
<span data-ttu-id="3d748-134">Bu değer ilke ifadeleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="3d748-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="3d748-135">Maksimum uzunluk 1000 karakterdir.</span><span class="sxs-lookup"><span data-stu-id="3d748-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="3d748-136">Değer boş olamaz veya yalnızca boşluklardan oluşamaz.</span><span class="sxs-lookup"><span data-stu-id="3d748-136">The value may not be empty or consist only of whitespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d748-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d748-137">CommonParameters</span></span>
<span data-ttu-id="3d748-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d748-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d748-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d748-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d748-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d748-140">INPUTS</span></span>

### <span data-ttu-id="3d748-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3d748-141">None</span></span>
<span data-ttu-id="3d748-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3d748-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d748-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d748-143">OUTPUTS</span></span>

### <span data-ttu-id="3d748-144">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="3d748-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="3d748-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d748-145">NOTES</span></span>

## <span data-ttu-id="3d748-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d748-146">RELATED LINKS</span></span>

[<span data-ttu-id="3d748-147">Get-Azurermapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="3d748-147">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="3d748-148">New-Azurermapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="3d748-148">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="3d748-149">Remove-Azurermapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="3d748-149">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)


